<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Tetris</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@700;800&family=Rubik+Mono+One&display=swap" rel="stylesheet">
<style>
*{box-sizing:border-box;margin:0}
:root{--bg:#f2eeff;--panel:#fff;--tx:#241a52;--mut:#6b61a3;--frame:#3a2b7c;--kb:#efeaff;--bd:#d9d0f5;--glow:#a66bff;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media(prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#130e2e;--panel:#1f1745;--tx:#f1edff;--mut:#a89fd8;--frame:#2d2166;--kb:#2c2260;--bd:#352a70}}
:root[data-theme="dark"]{--bg:#130e2e;--panel:#1f1745;--tx:#f1edff;--mut:#a89fd8;--frame:#2d2166;--kb:#2c2260;--bd:#352a70}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{min-height:100vh;display:grid;place-items:center;padding:16px;background:var(--bg);color:var(--tx);font:700 14px/1.4 Nunito,system-ui,-apple-system,"Segoe UI",sans-serif}
.app{display:grid;grid-template-columns:220px auto 230px;grid-template-areas:"left board nextp" "left board hints";grid-template-rows:auto 1fr;gap:20px;align-items:start}
.left{grid-area:left}.boardwrap{grid-area:board}.nextp{grid-area:nextp}.hints{grid-area:hints}.touch{grid-area:touch;display:none}
.panel{background:var(--panel);border:2px solid var(--bd);border-radius:20px;padding:18px}
small{display:block;font-size:13px;font-weight:800;color:var(--mut)}
h1{font:400 30px/1 "Rubik Mono One",Impact,sans-serif;margin-bottom:24px;text-shadow:0 3px 0 rgba(0,0,0,.22)}
.stats{display:grid;grid-template-columns:1fr 1fr;gap:16px 10px}
.stat b{display:block;font-size:26px;font-weight:800;line-height:1.15;font-variant-numeric:tabular-nums}
.stat.big{grid-column:1/-1}.stat.big b{font-size:34px}
.boardwrap{position:relative;padding:8px;border-radius:22px;background:var(--frame);box-shadow:0 0 0 3px var(--bd),0 0 56px -6px var(--glow);transition:box-shadow .45s}
#b{display:block;height:min(76vh,720px);height:min(76dvh,720px);aspect-ratio:1/2;border-radius:14px}
.ov{position:absolute;inset:8px;border-radius:14px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:14px;padding:22px;text-align:center;color:#f1edff;background:rgba(14,10,36,.84);backdrop-filter:blur(5px)}
.ov[hidden]{display:none}
.ov h2{font:400 28px/1.1 "Rubik Mono One",Impact,sans-serif}
.ov p{max-width:230px;color:#c9c0f2}.ov .s{font-size:13px;color:#8f85c4}
button{font:800 16px Nunito,system-ui,sans-serif;color:#fff;border:0;border-radius:14px;padding:12px 26px;cursor:pointer;background:#ff5368;box-shadow:0 5px 0 #b01e36;transition:transform .08s,box-shadow .08s}
button:active{transform:translateY(4px);box-shadow:0 1px 0 #b01e36}
button:focus-visible{outline:3px solid #fff;outline-offset:3px}
#toast{position:absolute;left:50%;top:34%;transform:translateX(-50%);font:400 26px "Rubik Mono One",Impact,sans-serif;color:#fff;white-space:nowrap;pointer-events:none;opacity:0;text-shadow:0 3px 0 #b01e36,0 0 24px var(--glow)}
#toast.pop{animation:pop .9s ease-out}
@keyframes pop{0%{opacity:0;transform:translate(-50%,14px) scale(.7)}20%{opacity:1;transform:translate(-50%,0) scale(1.08)}75%{opacity:1}100%{opacity:0;transform:translate(-50%,-34px) scale(1)}}
.nextp canvas{display:block;margin:10px auto 0;width:100%;max-width:150px;aspect-ratio:1;border-radius:14px;background:#0e0a24}
.hints ul{list-style:none;padding:0;margin:10px 0 14px}
.hints li{display:flex;align-items:center;justify-content:space-between;gap:10px;padding:5px 0}
kbd{display:inline-block;min-width:28px;text-align:center;font:800 13px Nunito,system-ui,sans-serif;padding:3px 8px;margin-left:4px;border-radius:8px;background:var(--kb);border:2px solid var(--bd);border-bottom-width:4px}
.tip{padding:12px 14px;border-radius:14px;background:var(--kb)}
.tip b{display:block;color:var(--mut);font-size:13px}
.touch{grid-template-columns:repeat(3,1fr);gap:10px;width:100%;max-width:420px;justify-self:center}
.touch button{padding:14px 0;font-size:20px;touch-action:manipulation;user-select:none;-webkit-user-select:none;background:#5584ff;box-shadow:0 5px 0 #2a4bb8}
.touch [data-a=cw],.touch [data-a=hd]{background:#ff5368;box-shadow:0 5px 0 #b01e36}
.touch [data-a=p]{background:#7a6fb8;box-shadow:0 5px 0 #4a3f85}
.touch [data-a=hd],.touch [data-a=p]{font-size:16px}
.prog{height:8px;border-radius:6px;background:var(--kb);overflow:hidden;margin-bottom:8px}
.prog i{display:block;height:100%;width:0;border-radius:6px;background:#4fdc74;transition:width .35s}
.ov svg{width:104px;height:104px;filter:drop-shadow(0 0 16px rgba(255,204,34,.55));animation:bob 2.2s ease-in-out infinite}
@keyframes bob{50%{transform:translateY(-6px)}}
.ov.win{background:rgba(14,10,36,.62);backdrop-filter:none}
@media(max-width:820px){
.app{grid-template-columns:1fr auto;grid-template-areas:"left nextp" "board board" "touch touch";grid-template-rows:auto;gap:12px;width:100%;max-width:440px}
.boardwrap{justify-self:center}
#b{height:min(54vh,560px);height:min(54dvh,560px)}
h1,.hints{display:none}.touch{display:grid}
.panel{padding:12px}
.stats{gap:8px 10px}.stat b,.stat.big b{font-size:22px}
.nextp canvas{width:84px}
#pl{display:none}
}
@media(prefers-reduced-motion:reduce){#toast{display:none}.boardwrap{transition:none}.ov svg{animation:none}}
</style>
</head>
<body>
<main class="app">
<section class="left panel">
<h1 id="logo" aria-label="Tetris"></h1>
<div class="stats">
<div class="stat big"><small>Pontuação</small><b id="sc">0</b></div>
<div class="stat big"><small>Recorde</small><b id="bs">0</b></div>
<div class="stat"><small>Nível</small><b id="lv">1</b></div>
<div class="stat"><small>Linhas</small><b id="ln">0</b></div>
<div class="stat big"><div class="prog"><i id="pg"></i></div><small id="pl"></small></div>
</div>
</section>
<div class="boardwrap" id="bw"><canvas id="b" aria-label="Tabuleiro do Tetris"></canvas><div id="toast"></div><div class="ov" id="ov"></div></div>
<section class="nextp panel"><small>Próxima peça</small><canvas id="n" width="150" height="150"></canvas></section>
<section class="hints panel">
<small>Controles</small>
<ul>
<li><span>Mover</span><span><kbd>←</kbd><kbd>→</kbd></span></li>
<li><span>Girar</span><span><kbd>↑</kbd><kbd>X</kbd></span></li>
<li><span>Girar ao contrário</span><kbd>Z</kbd></li>
<li><span>Descer devagar</span><kbd>↓</kbd></li>
<li><span>Queda total</span><kbd>Espaço</kbd></li>
<li><span>Pausar</span><kbd>P</kbd></li>
</ul>
<p class="tip"><b>Dica</b><span id="tip"></span></p>
</section>
<div class="touch">
<button data-a="l" aria-label="Esquerda">◀</button>
<button data-a="cw" aria-label="Girar">⟳</button>
<button data-a="r" aria-label="Direita">▶</button>
<button data-a="d" aria-label="Descer">▼</button>
<button data-a="hd">Queda</button>
<button data-a="p">Pausar</button>
</div>
</main>
<script>
(()=>{
const C=10,R=20,S=36,$=id=>document.getElementById(id);
const T={I:[[0,0,0,0],[1,1,1,1],[0,0,0,0],[0,0,0,0]],O:[[1,1],[1,1]],T:[[0,1,0],[1,1,1],[0,0,0]],S:[[0,1,1],[1,1,0],[0,0,0]],Z:[[1,1,0],[0,1,1],[0,0,0]],J:[[1,0,0],[1,1,1],[0,0,0]],L:[[0,0,1],[1,1,1],[0,0,0]]};
const K={I:['#9af3ff','#2fc6dd','#0b7f95'],O:['#fff0a0','#ffcc22','#b8860b'],T:['#dcc0ff','#a66bff','#5b2fb3'],S:['#b6ffc4','#4fdc74','#1b8a3c'],Z:['#ffb3bd','#ff5368','#b01e36'],J:['#b3c8ff','#5584ff','#2a4bb8'],L:['#ffd0a0','#ff9433','#b85a0c']};
const TIPS=['A peça fantasma, só com contorno, mostra onde ela vai cair.','Deixe uma coluna livre na borda e espere a peça I para fazer um Tetris.','Evite buracos: as peças S e Z se encaixam melhor em degraus.','Os pontos vêm só das linhas: limpar 4 de uma vez vale 800, o dobro de quatro linhas separadas.','Olhe a próxima peça antes de decidir onde encaixar a atual.','Uma pilha baixa e plana dá mais tempo para pensar quando a velocidade sobe.'];
const LG=[['T','Z'],['E','L'],['T','O'],['R','S'],['I','I'],['S','T']].map(([c,k])=>`<span style="color:${K[k][1]}">${c}</span>`).join('');
$('logo').innerHTML=LG;
const TR='<svg viewBox="0 0 96 96" aria-hidden="true"><path d="M26 18H12c0 16 6 26 18 29M70 18h14c0 16-6 26-18 29" fill="none" stroke="#ffcc22" stroke-width="6" stroke-linecap="round"/><path d="M26 12h44v22c0 14-9 25-22 25S26 48 26 34z" fill="#ffcc22"/><path d="M33 16h7v26c-5-3-7-9-7-16z" fill="#fff0a0" opacity=".75"/><path d="M48 22l3.5 7.2 7.9 1.1-5.7 5.6 1.4 7.9-7.1-3.8-7.1 3.8 1.4-7.9-5.7-5.6 7.9-1.1z" fill="#b8860b"/><rect x="43" y="58" width="10" height="14" fill="#e0a800"/><rect x="30" y="72" width="36" height="8" rx="3" fill="#e0a800"/><rect x="24" y="80" width="48" height="9" rx="3" fill="#b8860b"/></svg>';
const cv=$('b'),cx=cv.getContext('2d'),nx=$('n').getContext('2d');
cv.width=C*S;cv.height=R*S;
let b,cur,nxt,bag=[],score=0,lines=0,level=1,best=0,rec0=0,st='ready',last=0,acc=0,clr=null,tipN=0,conf=[];
try{best=+localStorage.getItem('tetris-best')||0}catch(e){}
const blank=()=>Array.from({length:R},()=>Array(C).fill(0));
const rr=(c,x,y,w,h,r)=>{c.beginPath();c.roundRect?c.roundRect(x,y,w,h,r):c.rect(x,y,w,h)};
const each=(m,f)=>m.forEach((r,j)=>r.forEach((v,i)=>v&&f(i,j)));
const rot=(m,d)=>d>0?m[0].map((_,i)=>m.map(r=>r[i]).reverse()):m[0].map((_,i)=>m.map(r=>r[r.length-1-i]));
const hit=(m,x,y)=>m.some((r,j)=>r.some((v,i)=>v&&(x+i<0||x+i>=C||y+j>=R||(y+j>=0&&b[y+j][x+i]))));
const ms=()=>Math.round(800*.78**(level-1));
const mv=(dx,dy)=>{if(!hit(cur.m,cur.x+dx,cur.y+dy)){cur.x+=dx;cur.y+=dy;return 1}return 0};
function rt(d){const m=rot(cur.m,d);for(const k of[0,-1,1,-2,2])if(!hit(m,cur.x+k,cur.y)){cur.m=m;cur.x+=k;return}}
function draw7(){if(!bag.length){bag=Object.keys(T);for(let i=6;i>0;i--){const j=Math.random()*(i+1)|0;[bag[i],bag[j]]=[bag[j],bag[i]]}}return bag.pop()}

function blk(c,x,y,s,t,a=1){
const[l,m,d]=K[t],p=s*.1;c.save();c.globalAlpha=a;
c.fillStyle=d;rr(c,x+1,y+1,s-2,s-2,s*.24);c.fill();
const g=c.createLinearGradient(0,y,0,y+s);g.addColorStop(0,l);g.addColorStop(.55,m);g.addColorStop(1,m);
c.fillStyle=g;rr(c,x+1+p,y+1+p*.6,s-2-2*p,s-2-p*1.8,s*.18);c.fill();
c.fillStyle='rgba(255,255,255,.45)';rr(c,x+s*.22,y+s*.2,s*.34,s*.1,s*.05);c.fill();c.restore()}

function render(){
const W=C*S,H=R*S;
cx.fillStyle='#0e0a24';cx.fillRect(0,0,W,H);
cx.fillStyle='rgba(255,255,255,.035)';
for(let y=0;y<R;y++)for(let x=0;x<C;x++)if((x+y)%2===0)cx.fillRect(x*S,y*S,S,S);
b.forEach((r,y)=>r.forEach((v,x)=>v&&blk(cx,x*S,y*S,S,v)));
if(cur){
if(st==='play'||st==='pause'){
let gy=cur.y;while(!hit(cur.m,cur.x,gy+1))gy++;
each(cur.m,(i,j)=>{cx.save();cx.strokeStyle=cx.fillStyle=K[cur.t][1];cx.lineWidth=2;rr(cx,(cur.x+i)*S+4,(gy+j)*S+4,S-8,S-8,7);cx.globalAlpha=.8;cx.stroke();cx.globalAlpha=.14;cx.fill();cx.restore()})}
cx.save();cx.shadowColor=K[cur.t][1];cx.shadowBlur=16;
each(cur.m,(i,j)=>cur.y+j>=0&&blk(cx,(cur.x+i)*S,(cur.y+j)*S,S,cur.t));cx.restore()}
if(clr){cx.fillStyle=`rgba(255,255,255,${Math.max(0,1-clr.t/260)})`;clr.rows.forEach(y=>cx.fillRect(0,y*S,W,S))}
if(st==='win')conf.forEach(p=>{p.x+=p.vx;p.y+=p.vy;p.a+=p.vr;if(p.y>H)p.y=-10;cx.save();cx.translate(p.x,p.y);cx.rotate(p.a);cx.fillStyle=p.c;cx.fillRect(-p.w/2,-p.w/4,p.w,p.w/2);cx.restore()})}

function drawNext(){
nx.clearRect(0,0,150,150);const c=[];each(T[nxt],(i,j)=>c.push([i,j]));
const xs=c.map(a=>a[0]),ys=c.map(a=>a[1]),x0=Math.min(...xs),y0=Math.min(...ys),w=Math.max(...xs)-x0+1,h=Math.max(...ys)-y0+1,s=30;
const ox=(150-w*s)/2-x0*s,oy=(150-h*s)/2-y0*s;
c.forEach(([i,j])=>blk(nx,ox+i*s,oy+j*s,s,nxt))}

function ui(){
if(score>best)best=score;
$('sc').textContent=score.toLocaleString('pt-BR');$('bs').textContent=best.toLocaleString('pt-BR');
$('lv').textContent=level;$('ln').textContent=lines;
const left=Math.max(0,level*1000-score);$('pg').style.width=(1000-left)/10+'%';
$('pl').textContent=`Faltam ${left.toLocaleString('pt-BR')} pontos ${level<10?'para o nível '+(level+1):'para zerar o jogo'}`}

function toast(t){if(!t)return;const e=$('toast');e.textContent=t;e.classList.remove('pop');void e.offsetWidth;e.classList.add('pop')}

function ov(k){
const o=$('ov');o.hidden=!k;o.classList.toggle('win',k==='win');if(!k)return;
const B=(t,h)=>`<button>${t}</button><p class="s">${h}</p>`;
o.innerHTML={
start:`<h2>${LG}</h2><p>Cada 1.000 pontos sobe um nível. Complete os 10 níveis para zerar o jogo.</p>${B('Jogar','Enter ou toque no botão')}`,
win:`${TR}<h2>Parabéns!</h2><p>Você zerou o Tetris: completou os 10 níveis com ${score.toLocaleString('pt-BR')} pontos.${score>rec0?' Novo recorde!':''}</p>${B('Jogar de novo','Enter')}`,
pause:`<h2>Pausado</h2>${B('Continuar','Tecla P')}`,
over:`<h2>Fim de jogo</h2><p>Você fez ${score.toLocaleString('pt-BR')} pontos.${score>rec0?' Novo recorde!':''}</p>${B('Jogar de novo','Enter')}`}[k]}

function spawn(){
const t=nxt;nxt=draw7();const m=T[t].map(r=>[...r]);
cur={t,m,x:(C-m[0].length)>>1,y:t==='I'?-1:0};
$('bw').style.setProperty('--glow',K[t][1]);drawNext();
if(hit(cur.m,cur.x,cur.y))over()}

function over(){st='over';try{localStorage.setItem('tetris-best',best)}catch(e){}ov('over')}

function lock(){
let out=0;each(cur.m,(i,j)=>{const y=cur.y+j;if(y<0)out=1;else b[y][cur.x+i]=cur.t});
if(out)return over();
if(++tipN%5===0)$('tip').textContent=TIPS[(tipN/5)%TIPS.length|0];
const rows=[];b.forEach((r,y)=>r.every(Boolean)&&rows.push(y));
if(rows.length){clr={rows,t:0};st='clear';cur=null}else spawn()}

function fin(){
const n=clr.rows.length,lv=level;
clr.rows.forEach(y=>{b.splice(y,1);b.unshift(Array(C).fill(0))});
score+=[0,100,300,500,800][n];lines+=n;level=Math.min(10,1+(score/1000|0));clr=null;ui();
if(score>=10000)return win();
toast(level>lv?'Nível '+level:['','Simples','Dupla','Tripla','Tetris!'][n]);
st='play';acc=0;spawn();ui()}

function win(){
st='win';cur=null;try{localStorage.setItem('tetris-best',best)}catch(e){}
conf=matchMedia('(prefers-reduced-motion:reduce)').matches?[]:Array.from({length:80},()=>({x:Math.random()*C*S,y:-Math.random()*R*S,vx:(Math.random()-.5)*2,vy:2+Math.random()*3,a:0,vr:(Math.random()-.5)*.3,w:8+Math.random()*8,c:K['IOTSZJL'[Math.random()*7|0]][1]}));
$('bw').style.setProperty('--glow','#ffcc22');ov('win')}

function start(){
b=blank();score=lines=0;level=1;bag=[];clr=null;conf=[];acc=0;rec0=best;
nxt=draw7();st='play';ov('');spawn();ui()}

function pause(){if(st==='play'){st='pause';ov('pause')}else if(st==='pause'){st='play';ov('')}}
const act=()=>{if(st==='pause')pause();else if(st==='ready'||st==='over'||st==='win')start()};

const A={
l:()=>mv(-1,0),r:()=>mv(1,0),
d:()=>{if(mv(0,1))acc=0},
cw:()=>rt(1),ccw:()=>rt(-1),
hd:()=>{while(mv(0,1));lock();acc=0}};

addEventListener('keydown',e=>{
const k=e.key.toLowerCase();
if(['arrowleft','arrowright','arrowdown','arrowup',' '].includes(k))e.preventDefault();
if(k==='enter'){act();return}
if(k==='p'||k==='escape'){pause();return}
if(st!=='play')return;
const a={arrowleft:'l',arrowright:'r',arrowdown:'d',arrowup:'cw',x:'cw',z:'ccw',' ':'hd'}[k];
if(a&&!(e.repeat&&(a==='cw'||a==='ccw'||a==='hd')))A[a]()});

$('ov').addEventListener('click',e=>{if(e.target.closest('button'))act()});
document.addEventListener('visibilitychange',()=>{if(document.hidden&&st==='play')pause()});

document.querySelectorAll('.touch button').forEach(el=>{
const a=el.dataset.a;let t,iv;
const stop=()=>{clearTimeout(t);clearInterval(iv)};
el.addEventListener('pointerdown',e=>{
e.preventDefault();
if(a==='p'){pause();return}
if(st!=='play')return;
A[a]();
if('lrd'.includes(a))t=setTimeout(()=>{iv=setInterval(()=>st==='play'&&A[a](),85)},190)});
['pointerup','pointerleave','pointercancel'].forEach(ev=>el.addEventListener(ev,stop))});

function loop(t){
const dt=Math.min(t-last,100);last=t;
if(st==='play'){acc+=dt;if(acc>=ms()){acc=0;if(!mv(0,1))lock()}}
else if(st==='clear'){clr.t+=dt;if(clr.t>260)fin()}
render();requestAnimationFrame(loop)}

b=blank();nxt=draw7();drawNext();ui();$('tip').textContent=TIPS[0];ov('start');
requestAnimationFrame(loop);
})();
</script>
</body>
</html>
