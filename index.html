<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>4v4 Team Deathmatch</title>

<style>
*{
    box-sizing:border-box;
    user-select:none;
}

html,body{
    margin:0;
    width:100%;
    height:100%;
    overflow:hidden;
    background:#111;
    font-family:Arial,sans-serif;
}

canvas{
    display:block;
    width:100%;
    height:100%;
}

/* ================= HUD ================= */

#hud{
    position:fixed;
    inset:0;
    pointer-events:none;
    color:white;
}

/* Score */

#scoreBoard{
    position:absolute;
    top:10px;
    left:50%;
    transform:translateX(-50%);
    display:flex;
    align-items:center;
    gap:14px;
    background:rgba(0,0,0,.55);
    border-radius:8px;
    padding:6px 18px;
    min-width:310px;
    justify-content:center;
}

.teamScore{
    font-size:24px;
    font-weight:bold;
}

.blue{
    color:#31a9ff;
}

.red{
    color:#ff4545;
}

#goal{
    font-size:11px;
    opacity:.8;
    text-align:center;
}

/* Mini map */

#map{
    position:absolute;
    top:15px;
    right:15px;
    width:180px;
    height:180px;
    background:rgba(15,25,30,.78);
    border:2px solid rgba(255,255,255,.4);
    border-radius:8px;
    overflow:hidden;
}

#mapCanvas{
    width:100%;
    height:100%;
}

/* Kill feed */

#killFeed{
    position:absolute;
    top:205px;
    right:18px;
    width:300px;
    text-align:right;
}

.kill{
    background:rgba(0,0,0,.48);
    padding:5px 9px;
    margin-bottom:4px;
    border-radius:4px;
    font-size:13px;
}

/* Ammo */

#ammo{
    position:absolute;
    right:25px;
    bottom:25px;
    font-size:28px;
    font-weight:bold;
    text-shadow:0 2px 4px black;
}

#weapon{
    position:absolute;
    right:28px;
    bottom:63px;
    font-size:14px;
    opacity:.85;
}

/* HP */

#hpBox{
    position:absolute;
    left:25px;
    bottom:28px;
    width:250px;
}

#hpBar{
    width:100%;
    height:13px;
    background:rgba(0,0,0,.65);
    border:1px solid white;
    border-radius:5px;
    overflow:hidden;
}

#hpFill{
    height:100%;
    width:100%;
    background:#29d85c;
}

/* Crosshair */

#crosshair{
    position:absolute;
    left:50%;
    top:50%;
    width:28px;
    height:28px;
    transform:translate(-50%,-50%);
}

#crosshair::before,
#crosshair::after{
    content:"";
    position:absolute;
    background:white;
    box-shadow:0 0 3px black;
}

#crosshair::before{
    width:28px;
    height:2px;
    top:13px;
}

#crosshair::after{
    width:2px;
    height:28px;
    left:13px;
}

/* Hit */

#hit{
    position:absolute;
    left:50%;
    top:50%;
    transform:translate(-50%,-50%);
    font-size:28px;
    color:white;
    opacity:0;
}

/* Message */

#message{
    position:absolute;
    top:75px;
    left:50%;
    transform:translateX(-50%);
    background:rgba(0,0,0,.55);
    padding:7px 15px;
    border-radius:7px;
    font-size:14px;
}

/* Buttons */

#buttons{
    position:absolute;
    right:20px;
    bottom:100px;
    display:flex;
    gap:8px;
    pointer-events:auto;
}

.btn{
    border:1px solid rgba(255,255,255,.35);
    background:rgba(20,20,20,.55);
    color:white;
    padding:10px 13px;
    border-radius:8px;
    font-weight:bold;
    cursor:pointer;
}

.btn.active{
    background:#1976d2;
}

/* Start */

#startScreen{
    position:fixed;
    inset:0;
    z-index:20;
    display:flex;
    justify-content:center;
    align-items:center;
    background:rgba(4,10,15,.9);
    color:white;
}

.startBox{
    width:390px;
    max-width:90%;
    background:rgba(15,20,25,.95);
    border:1px solid rgba(255,255,255,.2);
    border-radius:18px;
    padding:30px;
    text-align:center;
}

.startBox h1{
    margin-top:0;
}

#start{
    margin-top:20px;
    padding:14px 40px;
    background:#1687e8;
    border:0;
    border-radius:8px;
    color:white;
    font-size:18px;
    font-weight:bold;
    cursor:pointer;
}

/* Mobile */

#mobile{
    display:none;
    pointer-events:none;
}

#joystick{
    position:absolute;
    left:25px;
    bottom:30px;
    width:130px;
    height:130px;
    border:2px solid rgba(255,255,255,.35);
    border-radius:50%;
    background:rgba(0,0,0,.2);
    pointer-events:auto;
}

#knob{
    position:absolute;
    width:50px;
    height:50px;
    border-radius:50%;
    background:rgba(255,255,255,.45);
    left:38px;
    top:38px;
}

#fireButton{
    position:absolute;
    right:30px;
    bottom:35px;
    width:90px;
    height:90px;
    border-radius:50%;
    border:3px solid rgba(255,255,255,.7);
    background:rgba(210,35,35,.65);
    color:white;
    font-weight:bold;
    pointer-events:auto;
}

@media(pointer:coarse){
    #mobile{
        display:block;
        position:fixed;
        inset:0;
    }

    #buttons{
        display:none;
    }

    #map{
        width:135px;
        height:135px;
    }
}
</style>
</head>

<body>

<canvas id="game"></canvas>

<!-- ================= HUD ================= -->

<div id="hud">

    <div id="scoreBoard">
        <div class="teamScore blue" id="blueScore">0</div>

        <div id="goal">
            <b>TEAM DEATHMATCH</b><br>
            GOAL: 40
        </div>

        <div class="teamScore red" id="redScore">0</div>
    </div>

    <div id="map">
        <canvas id="mapCanvas" width="180" height="180"></canvas>
    </div>

    <div id="killFeed"></div>

    <div id="message">
        آماده نبرد
    </div>

    <div id="crosshair"></div>

    <div id="hit">✦</div>

    <div id="weapon">
        M416
    </div>

    <div id="ammo">
        <span id="magAmmo">40</span>
        /
        <span id="reserveAmmo">180</span>
    </div>

    <div id="hpBox">
        <div id="hpBar">
            <div id="hpFill"></div>
        </div>
    </div>

    <div id="buttons">
        <button class="btn" id="aimBtn">AIM</button>
        <button class="btn" id="crouchBtn">CROUCH</button>
        <button class="btn" id="reloadBtn">RELOAD</button>
    </div>

</div>

<!-- ================= MOBILE ================= -->

<div id="mobile">
    <div id="joystick">
        <div id="knob"></div>
    </div>

    <button id="fireButton">
        FIRE
    </button>
</div>

<!-- ================= START ================= -->

<div id="startScreen">

    <div class="startBox">

        <h1>4v4 TEAM DEATHMATCH</h1>

        <p>
            میدان نبرد شهری
        </p>

        <p style="opacity:.65;font-size:13px">
            WASD حرکت<br>
            Mouse دوربین<br>
            Left Click شلیک<br>
            Right Click Aim<br>
            Shift دویدن<br>
            C نشستن<br>
            R خشاب
        </p>

        <button id="start">
            START MATCH
        </button>

    </div>

</div>


<script type="module">

import * as THREE from
"https://cdn.jsdelivr.net/npm/three@0.180.0/build/three.module.js";


/* =========================================================
   BASIC
========================================================= */

const canvas =
document.getElementById("game");

const renderer =
new THREE.WebGLRenderer({
    canvas,
    antialias:true
});

renderer.setPixelRatio(
    Math.min(devicePixelRatio,1.6)
);

renderer.setSize(
    innerWidth,
    innerHeight
);

renderer.shadowMap.enabled = true;

renderer.shadowMap.type =
THREE.PCFSoftShadowMap;


const scene =
new THREE.Scene();

scene.background =
new THREE.Color(0x91a6ad);

scene.fog =
new THREE.Fog(
    0x91a6ad,
    45,
    120
);


/* =========================================================
   CAMERA
========================================================= */

const camera =
new THREE.PerspectiveCamera(
    70,
    innerWidth/innerHeight,
    .05,
    250
);

camera.position.set(
    0,
    2.2,
    22
);

scene.add(camera);


/* =========================================================
   LIGHT
========================================================= */

scene.add(
    new THREE.HemisphereLight(
        0xddefff,
        0x303840,
        2
    )
);

const sun =
new THREE.DirectionalLight(
    0xffffff,
    3
);

sun.position.set(
    20,
    35,
    15
);

sun.castShadow = true;

sun.shadow.mapSize.width = 2048;
sun.shadow.mapSize.height = 2048;

scene.add(sun);


/* =========================================================
   MATERIALS
========================================================= */

const groundMat =
new THREE.MeshStandardMaterial({
    color:0x4e5d58,
    roughness:.95
});

const concreteMat =
new THREE.MeshStandardMaterial({
    color:0x727a7b,
    roughness:.9
});

const darkConcrete =
new THREE.MeshStandardMaterial({
    color:0x3e4548,
    roughness:.95
});

const metalMat =
new THREE.MeshStandardMaterial({
    color:0x4a5053,
    metalness:.35,
    roughness:.7
});

const crateMat =
new THREE.MeshStandardMaterial({
    color:0x806341,
    roughness:1
});

const roofMat =
new THREE.MeshStandardMaterial({
    color:0x353b3c,
    roughness:1
});

const blueMat =
new THREE.MeshStandardMaterial({
    color:0x177bd1
});

const redMat =
new THREE.MeshStandardMaterial({
    color:0xd62e37
});


/* =========================================================
   GROUND
========================================================= */

const ground =
new THREE.Mesh(
    new THREE.PlaneGeometry(
        100,
        100
    ),
    groundMat
);

ground.rotation.x =
-Math.PI/2;

ground.receiveShadow = true;

scene.add(ground);


/* =========================================================
   MAP HELPERS
========================================================= */

const obstacles = [];


function box(
    x,
    y,
    z,
    w,
    h,
    d,
    material,
    collidable=true
){

    const mesh =
    new THREE.Mesh(
        new THREE.BoxGeometry(
            w,
            h,
            d
        ),
        material
    );

    mesh.position.set(
        x,
        y + h/2,
        z
    );

    mesh.castShadow = true;
    mesh.receiveShadow = true;

    scene.add(mesh);

    if(collidable){
        obstacles.push(mesh);
    }

    return mesh;
}


/* =========================================================
   OUTER WALLS
========================================================= */

box(
    0,
    0,
    -32,
    68,
    4,
    2,
    concreteMat
);

box(
    0,
    0,
    32,
    68,
    4,
    2,
    concreteMat
);

box(
    -34,
    0,
    0,
    2,
    4,
    64,
    concreteMat
);

box(
    34,
    0,
    0,
    2,
    4,
    64,
    concreteMat
);


/* =========================================================
   CENTRAL BUILDING
========================================================= */

/* main central structure */

box(
    0,
    0,
    0,
    18,
    5,
    13,
    darkConcrete
);


/* upper roof */

box(
    0,
    5,
    0,
    20,
    1,
    15,
    roofMat
);


/* central openings */

box(
    -10,
    0,
    -7,
    3,
    3,
    2,
    concreteMat
);

box(
    10,
    0,
    -7,
    3,
    3,
    2,
    concreteMat
);

box(
    -10,
    0,
    7,
    3,
    3,
    2,
    concreteMat
);

box(
    10,
    0,
    7,
    3,
    3,
    2,
    concreteMat
);


/* =========================================================
   SIDE LANES
========================================================= */

/* left lane */

box(
    -23,
    0,
    -15,
    12,
    2.8,
    2.2,
    concreteMat
);

box(
    -23,
    0,
    15,
    12,
    2.8,
    2.2,
    concreteMat
);


/* right lane */

box(
    23,
    0,
    -15,
    12,
    2.8,
    2.2,
    concreteMat
);

box(
    23,
    0,
    15,
    12,
    2.8,
    2.2,
    concreteMat
);


/* =========================================================
   MID COVER
========================================================= */

const covers = [

    [-16, -8, 4, 2, 2],
    [16, -8, 4, 2, 2],

    [-16, 8, 4, 2, 2],
    [16, 8, 4, 2, 2],

    [-6, -12, 3, 2, 2],
    [6, -12, 3, 2, 2],

    [-6, 12, 3, 2, 2],
    [6, 12, 3, 2, 2],

    [-21, 0, 3, 2, 2],
    [21, 0, 3, 2, 2],

    [-3, 20, 4, 2, 2],
    [3, 20, 4, 2, 2],

    [-3, -20, 4, 2, 2],
    [3, -20, 4, 2, 2]
];

covers.forEach(
    p=>box(
        p[0],
        0,
        p[1],
        p[2],
        p[3],
        p[4],
        concreteMat
    )
);


/* =========================================================
   CRATES
========================================================= */

const crates = [

    [-27,-22],
    [-22,-22],
    [22,-22],
    [27,-22],

    [-27,22],
    [-22,22],
    [22,22],
    [27,22],

    [-28,-5],
    [28,-5],
    [-28,5],
    [28,5]
];

crates.forEach(
    p=>{
        box(
            p[0],
            0,
            p[1],
            2.5,
            2,
            2.5,
            crateMat
        );

        box(
            p[0],
            2,
            p[1],
            2.5,
            .25,
            2.5,
            metalMat,
            false
        );
    }
);


/* =========================================================
   SMALL BUILDINGS
========================================================= */

function smallBuilding(x,z){

    box(
        x,
        0,
        z,
        7,
        3.5,
        6,
        concreteMat
    );

    box(
        x,
        3.5,
        z,
        7.5,
        .7,
        6.5,
        roofMat,
        false
    );

}

smallBuilding(-25,-12);
smallBuilding(25,-12);
smallBuilding(-25,12);
smallBuilding(25,12);


/* =========================================================
   SPAWN ZONES
========================================================= */

function spawnPad(x,z,material){

    const pad =
    new THREE.Mesh(
        new THREE.BoxGeometry(
            10,
            .15,
            8
        ),
        material
    );

    pad.position.set(
        x,
        .08,
        z
    );

    scene.add(pad);
}

spawnPad(
    0,
    -27,
    new THREE.MeshBasicMaterial({
        color:0x145c9b,
        transparent:true,
        opacity:.55
    })
);

spawnPad(
    0,
    27,
    new THREE.MeshBasicMaterial({
        color:0x98252b,
        transparent:true,
        opacity:.55
    })
);


/* =========================================================
   PLAYER
========================================================= */

const player =
new THREE.Group();

scene.add(player);

player.position.set(
    0,
    0,
    -27
);


/* player body */

const body =
new THREE.Mesh(
    new THREE.BoxGeometry(
        .7,
        1.2,
        .45
    ),
    blueMat
);

body.position.y = 1.2;

body.castShadow = true;

player.add(body);


/* head */

const head =
new THREE.Mesh(
    new THREE.SphereGeometry(
        .28,
        16,
        12
    ),
    new THREE.MeshStandardMaterial({
        color:0xd9a77d
    })
);

head.position.y = 2;

head.castShadow = true;

player.add(head);


/* =========================================================
   GUN
========================================================= */

const gun =
new THREE.Group();

const gunMat =
new THREE.MeshStandardMaterial({
    color:0x151719,
    metalness:.7,
    roughness:.25
});

const receiver =
new THREE.Mesh(
    new THREE.BoxGeometry(
        .28,
        .25,
        .8
    ),
    gunMat
);

receiver.position.set(
    .55,
    1.45,
    -.45
);

gun.add(receiver);


const barrel =
new THREE.Mesh(
    new THREE.CylinderGeometry(
        .045,
        .045,
        .9,
        12
    ),
    gunMat
);

barrel.rotation.x =
Math.PI/2;

barrel.position.set(
    .55,
    1.45,
    -1
);

gun.add(barrel);

camera.add(gun);


/* =========================================================
   ENEMIES
========================================================= */

const enemies = [];


function createEnemy(
    x,
    z
){

    const enemy =
    new THREE.Group();

    enemy.position.set(
        x,
        0,
        z
    );

    const ebody =
    new THREE.Mesh(
        new THREE.BoxGeometry(
            .72,
            1.2,
            .46
        ),
        redMat
    );

    ebody.position.y = 1.2;

    ebody.castShadow = true;

    enemy.add(ebody);


    const ehead =
    new THREE.Mesh(
        new THREE.SphereGeometry(
            .28,
            16,
            12
        ),
        new THREE.MeshStandardMaterial({
            color:0xd9a77d
        })
    );

    ehead.position.y = 2;

    ehead.castShadow = true;

    enemy.add(ehead);


    enemy.userData = {
        hp:100,
        maxHp:100,
        dead:false,
        cooldown:Math.random()*2
    };


    scene.add(enemy);

    enemies.push(enemy);

    return enemy;
}


/* enemy spawn */

createEnemy(-7,27);
createEnemy(7,27);
createEnemy(-14,23);
createEnemy(14,23);


/* =========================================================
   FRIENDLY TEAM VISUALS
========================================================= */

const teammates = [];

function createTeammate(x,z){

    const t =
    new THREE.Group();

    t.position.set(
        x,
        0,
        z
    );

    const b =
    new THREE.Mesh(
        new THREE.BoxGeometry(
            .7,
            1.2,
            .45
        ),
        blueMat
    );

    b.position.y=1.2;

    t.add(b);


    const h =
    new THREE.Mesh(
        new THREE.SphereGeometry(
            .27,
            14,
            10
        ),
        new THREE.MeshStandardMaterial({
            color:0xd9a77d
        })
    );

    h.position.y=2;

    t.add(h);

    scene.add(t);

    teammates.push(t);
}

createTeammate(-8,-24);
createTeammate(8,-24);
createTeammate(0,-22);


/* =========================================================
   GAME VARIABLES
========================================================= */

const keys = {};

let yaw = 0;
let pitch = 0;

let started = false;

let aiming = false;
let crouching = false;

let ammo = 40;
let reserve = 180;

let hp = 100;

let blueScore = 0;
let redScore = 0;

let shootCooldown = 0;

let reloadTimer = 0;

let playerDead = false;


/* =========================================================
   INPUT
========================================================= */

addEventListener(
    "keydown",
    e=>{
        keys[
            e.key.toLowerCase()
        ] = true;

        if(e.code==="KeyR")
            reload();

        if(e.code==="KeyC")
            crouching=!crouching;

        if(e.code==="ShiftLeft")
            keys.shift=true;
    }
);

addEventListener(
    "keyup",
    e=>{
        keys[
            e.key.toLowerCase()
        ] = false;
    }
);


/* =========================================================
   CAMERA
========================================================= */

function look(dx,dy){

    yaw -= dx*.0025;

    pitch -= dy*.0025;

    pitch =
    Math.max(
        -1.15,
        Math.min(
            1.15,
            pitch
        )
    );
}


canvas.addEventListener(
    "click",
    ()=>{
        if(started)
            canvas.requestPointerLock?.();
    }
);


document.addEventListener(
    "mousemove",
    e=>{
        if(
            document.pointerLockElement
            ===canvas
        ){
            look(
                e.movementX,
                e.movementY
            );
        }
    }
);


/* =========================================================
   AIM
========================================================= */

function setAim(value){

    aiming=value;

    camera.fov =
    aiming ? 52 : 70;

    camera.updateProjectionMatrix();

    document
    .getElementById("aimBtn")
    .classList.toggle(
        "active",
        aiming
    );
}

document
.getElementById("aimBtn")
.onclick=()=>{
    setAim(!aiming);
};


addEventListener(
    "mousedown",
    e=>{

        if(e.button===0)
            shoot();

        if(e.button===2)
            setAim(true);

    }
);

addEventListener(
    "mouseup",
    e=>{
        if(e.button===2)
            setAim(false);
    }
);

document.addEventListener(
    "contextmenu",
    e=>e.preventDefault()
);


/* =========================================================
   MOVEMENT COLLISION
========================================================= */

function blocked(
    position
){

    const p =
    new THREE.Vector3(
        position.x,
        1,
        position.z
    );

    return obstacles.some(
        o=>{
            const b =
            new THREE.Box3()
            .setFromObject(o);

            b.expandByScalar(.65);

            return b.containsPoint(p);
        }
    );
}


/* =========================================================
   SHOOT
========================================================= */

const ray =
new THREE.Raycaster();


function shoot(){

    if(!started)
        return;

    if(playerDead)
        return;

    if(reloadTimer>0)
        return;

    if(shootCooldown>0)
        return;

    if(ammo<=0){

        message(
            "خشاب خالی - R"
        );

        return;
    }

    ammo--;

    shootCooldown=.11;

    updateAmmo();


    /* muzzle flash */

    const flash =
    new THREE.PointLight(
        0xffc45c,
        6,
        3
    );

    flash.position.set(
        .55,
        1.45,
        -1.2
    );

    gun.add(flash);

    setTimeout(
        ()=>{
            gun.remove(flash);
        },
        35
    );


    ray.setFromCamera(
        new THREE.Vector2(0,0),
        camera
    );


    const targets=[];

    enemies.forEach(
        e=>{
            if(!e.userData.dead)
                targets.push(...e.children);
        }
    );


    const hits =
    ray.intersectObjects(
        targets,
        true
    );


    if(hits.length){

        let target =
        hits[0].object;

        while(
            target.parent &&
            !target.userData.hp
        ){
            target =
            target.parent;
        }


        if(target.userData.hp){

            target.userData.hp -= 34;

            showHit();


            if(
                target.userData.hp<=0
            ){

                target.userData.dead=true;

                target.visible=false;

                blueScore++;

                updateScore();

                addKill(
                    "YOU",
                    "ENEMY"
                );

                setTimeout(
                    ()=>{
                        respawnEnemy(
                            target
                        );
                    },
                    2500
                );
            }

        }

    }

}


/* =========================================================
   ENEMY RESPAWN
========================================================= */

function respawnEnemy(enemy){

    enemy.userData.hp=100;

    enemy.userData.dead=false;

    enemy.visible=true;

    enemy.position.set(
        (Math.random()>.5?1:-1)
        *(6+Math.random()*9),
        0,
        23+Math.random()*4
    );
}


/* =========================================================
   ENEMY AI
========================================================= */

function enemyAI(
    enemy,
    dt
){

    if(enemy.userData.dead)
        return;


    const dx =
    player.position.x -
    enemy.position.x;

    const dz =
    player.position.z -
    enemy.position.z;

    const distance =
    Math.hypot(
        dx,
        dz
    );


    if(distance>7){

        enemy.position.x +=
        dx/distance*
        dt*.9;

        enemy.position.z +=
        dz/distance*
        dt*.9;

    }


    enemy.lookAt(
        player.position.x,
        1.2,
        player.position.z
    );


    enemy.userData.cooldown -= dt;


    if(
        distance<28 &&
        enemy.userData.cooldown<=0
    ){

        enemy.userData.cooldown =
        1.2+Math.random()*1.4;

        if(
            Math.random()<.35
        ){

            hp-=10;

            updateHP();

            if(hp<=0)
                playerDeath();
        }
    }

}


/* =========================================================
   PLAYER DEATH
========================================================= */

function playerDeath(){

    if(playerDead)
        return;

    playerDead=true;

    redScore++;

    updateScore();

    message(
        "☠️ شما کشته شدید"
    );

    setTimeout(
        ()=>{
            player.position.set(
                (Math.random()-.5)*5,
                0,
                -26
            );

            hp=100;

            playerDead=false;

            updateHP();

            message(
                "بازگشت به میدان"
            );
        },
        2200
    );
}


/* =========================================================
   UI
========================================================= */

function updateScore(){

    document
    .getElementById("blueScore")
    .textContent=blueScore;

    document
    .getElementById("redScore")
    .textContent=redScore;


    if(
        blueScore>=40 ||
        redScore>=40
    ){

        message(
            blueScore>=40
            ? "🏆 تیم آبی پیروز شد!"
            : "🔴 تیم قرمز پیروز شد!"
        );

    }

}


function updateHP(){

    document
    .getElementById("hpFill")
    .style.width =
    Math.max(
        0,
        hp
    )+"%";
}


function updateAmmo(){

    document
    .getElementById("magAmmo")
    .textContent=ammo;

    document
    .getElementById("reserveAmmo")
    .textContent=reserve;
}


function message(text){

    document
    .getElementById("message")
    .textContent=text;
}


function showHit(){

    const h =
    document.getElementById("hit");

    h.style.opacity=1;

    setTimeout(
        ()=>{
            h.style.opacity=0;
        },
        100
    );
}


function addKill(
    killer,
    victim
){

    const feed =
    document
    .getElementById("killFeed");

    const item =
    document.createElement("div");

    item.className="kill";

    item.innerHTML =
    `<span class="blue">${killer}</span>
     🔫
     <span class="red">${victim}</span>`;

    feed.prepend(item);

    setTimeout(
        ()=>{
            item.remove();
        },
        3500
    );
}


/* =========================================================
   RELOAD
========================================================= */

function reload(){

    if(
        reloadTimer>0 ||
        ammo>=40 ||
        reserve<=0
    )
        return;

    reloadTimer=1.3;

    message(
        "↻ در حال تعویض خشاب..."
    );

    setTimeout(
        ()=>{

            const amount =
            Math.min(
                40-ammo,
                reserve
            );

            ammo += amount;

            reserve -= amount;

            reloadTimer=0;

            updateAmmo();

            message(
                "خشاب آماده"
            );

        },
        1300
    );
}

document
.getElementById("reloadBtn")
.onclick=reload;


document
.getElementById("crouchBtn")
.onclick=()=>{
    crouching=!crouching;

    document
    .getElementById("crouchBtn")
    .classList.toggle(
        "active",
        crouching
    );
};


/* =========================================================
   MINIMAP
========================================================= */

const mapCanvas =
document.getElementById(
    "mapCanvas"
);

const mapCtx =
mapCanvas.getContext("2d");


function drawMap(){

    const w=180;
    const h=180;

    mapCtx.clearRect(
        0,
        0,
        w,
        h
    );


    mapCtx.fillStyle="#293234";

    mapCtx.fillRect(
        0,
        0,
        w,
        h
    );


    /* central building */

    mapCtx.fillStyle="#596263";

    mapCtx.fillRect(
        71,
        55,
        38,
        70
    );


    /* covers */

    mapCtx.fillStyle="#8c9291";

    for(
        let i=0;
        i<10;
        i++
    ){

        const x=
        20+
        Math.random()*140;

    }


    /* player */

    const px =
    90+
    player.position.x*
    2.4;

    const py =
    90+
    player.position.z*
    2.4;

    mapCtx.fillStyle="#31a9ff";

    mapCtx.beginPath();

    mapCtx.arc(
        px,
        py,
        5,
        0,
        Math.PI*2
    );

    mapCtx.fill();


    /* enemies */

    enemies.forEach(
        e=>{

            if(e.userData.dead)
                return;

            const x=
            90+
            e.position.x*
            2.4;

            const y=
            90+
            e.position.z*
            2.4;

            mapCtx.fillStyle="#ff4040";

            mapCtx.beginPath();

            mapCtx.arc(
                x,
                y,
                4,
                0,
                Math.PI*2
            );

            mapCtx.fill();

        }
    );

}


/* =========================================================
   MOBILE JOYSTICK
========================================================= */

let joyX=0;
let joyY=0;

let joyActive=false;

const joystick =
document.getElementById(
    "joystick"
);

const knob =
document.getElementById(
    "knob"
);


joystick.addEventListener(
    "pointerdown",
    e=>{
        joyActive=true;

        joystick.setPointerCapture(
            e.pointerId
        );
    }
);


joystick.addEventListener(
    "pointermove",
    e=>{

        if(!joyActive)
            return;

        const r =
        joystick.getBoundingClientRect();

        let x =
        e.clientX -
        (
            r.left+
            r.width/2
        );

        let y =
        e.clientY -
        (
            r.top+
            r.height/2
        );

        const max=40;

        const len =
        Math.hypot(x,y);

        if(len>max){

            x=x/len*max;
            y=y/len*max;

        }

        joyX=x/max;
        joyY=y/max;

        knob.style.transform=
        `translate(${x}px,${y}px)`;

    }
);


joystick.addEventListener(
    "pointerup",
    ()=>{
        joyActive=false;
        joyX=0;
        joyY=0;
        knob.style.transform="";
    }
);


document
.getElementById(
    "fireButton"
)
.addEventListener(
    "pointerdown",
    shoot
);


/* =========================================================
   START
========================================================= */

document
.getElementById("start")
.onclick=()=>{

    started=true;

    document
    .getElementById(
        "startScreen"
    )
    .style.display="none";

    canvas.requestPointerLock?.();

    message(
        "🔥 MATCH START"
    );

};


/* =========================================================
   CLOCK
========================================================= */

const clock =
new THREE.Clock();


/* =========================================================
   MAIN LOOP
========================================================= */

function loop(){

    requestAnimationFrame(loop);

    const dt =
    Math.min(
        clock.getDelta(),
        .05
    );


    shootCooldown =
    Math.max(
        0,
        shootCooldown-dt
    );


    if(started){

        /* =====================================
           PLAYER MOVEMENT
        ===================================== */

        let forwardInput =
        (keys.w?1:0) -
        (keys.s?1:0) -
        joyY;

        let sideInput =
        (keys.d?1:0) -
        (keys.a?1:0) +
        joyX;


        let speed =
        keys.shift
        ? 9
        : crouching
        ? 3
        : 5.5;


        if(playerDead)
            speed=0;


        const forward =
        new THREE.Vector3(
            Math.sin(yaw),
            0,
            Math.cos(yaw)
        );


        const right =
        new THREE.Vector3(
            Math.cos(yaw),
            0,
            -Math.sin(yaw)
        );


        const next =
        player.position
        .clone()
        .addScaledVector(
            forward,
            -forwardInput*
            speed*dt
        )
        .addScaledVector(
            right,
            sideInput*
            speed*dt
        );


        if(!blocked(next)){

            player.position.x=
            next.x;

            player.position.z=
            next.z;

        }


        player.position.x=
        THREE.MathUtils.clamp(
            player.position.x,
            -30,
            30
        );

        player.position.z=
        THREE.MathUtils.clamp(
            player.position.z,
            -29,
            29
        );


        /* =====================================
           CAMERA TPP
        ===================================== */

        const height =
        crouching
        ? 1.55
        : 2.05;


        const cameraDistance =
        aiming
        ? 2.2
        : 5.2;


        const cameraTarget =
        new THREE.Vector3(
            player.position.x,
            height,
            player.position.z
        );


        const cameraOffset =
        new THREE.Vector3(
            Math.sin(yaw)*
            cameraDistance,
            .7,
            Math.cos(yaw)*
            cameraDistance
        );


        const desired =
        cameraTarget
        .clone()
        .add(cameraOffset);


        camera.position.lerp(
            desired,
            .18
        );


        camera.lookAt(
            cameraTarget
        );


        /* =====================================
           ENEMY AI
        ===================================== */

        enemies.forEach(
            e=>enemyAI(e,dt)
        );


        /* =====================================
           MAP
        ===================================== */

        drawMap();

    }


    renderer.render(
        scene,
        camera
    );

}

loop();


/* =========================================================
   RESIZE
========================================================= */

addEventListener(
    "resize",
    ()=>{

        camera.aspect =
        innerWidth/
        innerHeight;

        camera.updateProjectionMatrix();

        renderer.setSize(
            innerWidth,
            innerHeight
        );

    }
);


/* =========================================================
   INITIAL UI
========================================================= */

updateAmmo();
updateHP();
updateScore();

</script>

</body>
</html>
