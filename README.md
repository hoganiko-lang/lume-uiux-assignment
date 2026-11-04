[index.html](https://github.com/user-attachments/files/34361102/index.html)
<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>L Message｜AI顧客プロファイル（couleur）</title>
<style>
:root{--g:#08bf5a;--gd:#06a04b;--gl:#e7f8ee;--tx:#222;--mu:#6b7280;--bd:#e5e7eb;--bg:#f0f2f5;--sf:#fff;--sf2:#f3f4f6;--bl:#2b7de9;--bll:#e8f1fd;--bub:#f1f3f5;--wa:#f59e0b;--wal:#fff4de;--rd:#ef4444;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
/* ===== カラーテーマ（CSS変数で一括切り替え） ===== */
:root[data-theme="dark"]{color-scheme:dark;--tx:#d4d4d4;--mu:#8b949e;--bd:#343841;--bg:#1e1e1e;--sf:#252526;--sf2:#2d2d30;--g:#10c96a;--gd:#3ddc84;--gl:#173d2c;--bl:#5ea6ff;--bll:#1f3a5c;--bub:#2d2d30;--wa:#e5a93a;--wal:#3a2d10;--rd:#f06a6a}
:root[data-theme="sage"]{--tx:#2b3a2f;--mu:#6b7d6f;--bd:#d6e1d2;--bg:#e8eee3;--sf:#f8faf5;--sf2:#edf2e9;--g:#5f8f5a;--gd:#456f41;--gl:#dde9d6;--bl:#4a7a46;--bll:#dbe7d3;--bub:#e9efe4;--wa:#b98a2e;--wal:#f4ead0;--rd:#c8624f}
:root[data-theme="lavender"]{--tx:#3a2f45;--mu:#86758f;--bd:#eadff0;--bg:#f4edf7;--sf:#fffbff;--sf2:#f7eefa;--g:#a35fc0;--gd:#85429f;--gl:#f2e2f8;--bl:#9a52b8;--bll:#efe0f5;--bub:#f6ecf9;--wa:#d08a3c;--wal:#fdebe0;--rd:#d9566e}
body,.side,.top,.card,.acc,.ib,.btn,.nv,.fi,.bb,.sel,.modal,.box,.tag,.thm{transition:background-color .3s,border-color .3s,color .3s}
.th{position:relative}.thm{position:absolute;right:0;top:48px;width:250px;background:var(--sf);border:1px solid var(--bd);border-radius:12px;box-shadow:0 10px 28px rgba(0,0,0,.22);padding:8px;z-index:60}
.thm h4{margin:6px 10px 8px;font-size:11px;color:var(--mu);font-weight:600}
.to{display:flex;align-items:center;gap:10px;padding:9px 10px;border-radius:8px;width:100%;text-align:left;font-size:13px}.to:hover{background:var(--sf2)}.to.on{background:var(--gl)}
.to small{display:block;color:var(--mu);font-size:11px}.to .ck{margin-left:auto;color:var(--g);font-weight:700}
.sw{width:30px;height:30px;border-radius:50%;border:1px solid var(--bd);flex-shrink:0}
*{box-sizing:border-box}html,body{height:100%;margin:0}
body{font-family:"Hiragino Sans","Noto Sans JP","Yu Gothic",system-ui,sans-serif;color:var(--tx);background:var(--bg);font-size:14px;min-width:1200px;overflow:hidden}
button{font:inherit;cursor:pointer;border:0;background:none;color:inherit;padding:0}svg{flex-shrink:0}
.app{display:flex;height:100%}
.side{width:220px;background:var(--sf);border-right:1px solid var(--bd);overflow:auto;padding-bottom:20px;flex-shrink:0}
.logo{display:flex;align-items:center;gap:8px;font-weight:800;font-size:22px;color:var(--g);padding:14px 20px;height:58px;letter-spacing:.5px}
.logo i{width:28px;height:28px;border-radius:50%;background:var(--g);color:#fff;display:grid;place-items:center;font-size:14px;font-style:normal}
.sl{font-size:11px;color:var(--mu);padding:14px 14px 6px}
.nv{display:flex;align-items:center;gap:10px;margin:2px 6px;padding:10px 12px;border-radius:8px;font-size:13px;cursor:pointer}
.nv:hover{background:var(--sf2)}.nv.on{background:var(--bll);color:var(--bl)}.nv .ch{margin-left:auto;color:var(--mu)}
.main{flex:1;display:flex;flex-direction:column;min-width:0}
.top{height:58px;background:var(--sf);border-bottom:1px solid var(--bd);display:flex;align-items:center;gap:12px;padding:0 16px;flex-shrink:0}
.acc{display:flex;align-items:center;gap:10px;border:1px solid var(--bd);border-radius:8px;padding:6px 12px;width:230px;font-size:13px}
.acc .ch{margin-left:auto}
.sa{width:28px;height:28px;border-radius:50%;background:#f6f1e3 url(data:image/jpeg;base64,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) center/cover no-repeat;border:1px solid var(--bd);color:transparent;font-size:0;overflow:hidden}
.ib{border:1px solid var(--bd);border-radius:8px;width:38px;height:38px;display:grid;place-items:center}
.demo{margin-left:auto;display:flex;background:var(--sf2);padding:3px;border-radius:9px;gap:2px}
.demo button{padding:6px 12px;border-radius:7px;font-size:12px;color:var(--mu)}.demo button.on{background:var(--sf);color:var(--tx);font-weight:700;box-shadow:0 1px 3px rgba(0,0,0,.15)}
.up{border:1px solid var(--bl);color:var(--bl);border-radius:6px;padding:7px 12px;font-size:13px;display:flex;gap:6px;align-items:center}
.ti{display:flex;flex-direction:column;align-items:center;font-size:10px;color:var(--mu);gap:2px;padding:0 6px}
.view{flex:1;min-height:0;display:none;padding:16px;gap:16px}.view.on{display:flex}
#v-list{flex-direction:column;overflow:auto}
.card{background:var(--sf);border-radius:12px;border:1px solid var(--bd)}
.btn{padding:8px 16px;border-radius:8px;border:1px solid var(--bd);background:var(--sf);font-weight:600;font-size:13px}
.btn.pri{background:var(--g);border-color:var(--g);color:#fff}.btn.pri:hover{background:var(--gd)}
.row{display:flex;align-items:center;gap:10px}
/* list */
.stats{display:grid;grid-template-columns:repeat(4,1fr);gap:16px}
.stat{padding:16px}.stat small{color:var(--mu)}.stat b{display:block;font-size:24px;margin-top:4px}
.chips{display:flex;gap:8px;padding:14px 16px;border-bottom:1px solid var(--bd);align-items:center}
.chip{padding:5px 12px;border-radius:99px;border:1px solid var(--bd);font-size:13px;color:var(--mu)}.chip.on{background:var(--g);border-color:var(--g);color:#fff}
input.s{margin-left:auto;padding:7px 12px;border:1px solid var(--bd);border-radius:8px;width:240px;background:var(--sf2);color:var(--tx);font:inherit}
table{width:100%;border-collapse:collapse}th{text-align:left;font-size:12px;color:var(--mu);font-weight:600;padding:10px 16px;background:var(--sf2)}
td{padding:14px 16px;border-top:1px solid var(--bd);vertical-align:middle}tr.fr{cursor:pointer}tr.fr:hover td{background:var(--sf2)}
.av{width:40px;height:40px;border-radius:50%;display:grid;place-items:center;color:#fff;font-weight:700;flex-shrink:0}
.tag{display:inline-block;padding:2px 9px;border-radius:99px;font-size:12px;margin:2px 4px 2px 0;background:var(--gl);color:var(--gd);font-weight:600}
.tag.w{background:var(--wal);color:var(--wa)}.tag.n{background:var(--bll);color:var(--bl)}.tag.new{animation:pop .6s}
@keyframes pop{0%{transform:scale(.6);opacity:0}60%{transform:scale(1.15)}100%{transform:scale(1);opacity:1}}
.sum{color:var(--mu);font-size:13px;line-height:1.5;max-width:340px}
.bar{height:6px;border-radius:9px;background:var(--bd);overflow:hidden;flex:1}.bar span{display:block;height:100%;background:var(--g);border-radius:9px}
.score{display:flex;align-items:center;gap:8px;font-weight:700}
/* chat 3col */
.fl{width:260px;display:flex;flex-direction:column;flex-shrink:0;overflow:hidden}
.fl-t{padding:12px;display:flex;gap:8px}.fl-t .dd{flex:1;background:var(--sf2);border-radius:8px;padding:9px 12px;font-size:12px;display:flex;justify-content:space-between;align-items:center}
.fl-t .ib{width:36px;height:36px;background:var(--sf2);border:0}
.fl-s{margin:0 12px 6px;background:var(--sf2);border-radius:8px;padding:9px 12px;display:flex;gap:8px;color:var(--mu);font-size:13px;align-items:center}
.fl-s input{border:0;background:none;outline:0;font:inherit;color:var(--tx);width:100%}
.fl-b{flex:1;overflow:auto}
.fi{display:flex;gap:10px;padding:14px 12px;cursor:pointer;position:relative}.fi:hover,.fi.on{background:var(--sf2)}
.fi .mid{flex:1;min-width:0}.fi b{font-size:13px;font-weight:500}.fi .pv{color:var(--mu);font-size:12px;margin-top:3px;margin-bottom:14px;padding-right:44px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.fi .tm{position:absolute;right:12px;bottom:10px;font-size:11px;color:var(--mu)}
.ub{position:absolute;right:12px;top:14px;background:var(--rd);color:#fff;border-radius:99px;min-width:18px;height:18px;display:grid;place-items:center;font-size:11px;font-weight:700;padding:0 5px}
.fl-f{border-top:1px solid var(--bd);padding:8px 12px;display:flex;align-items:center;gap:10px;font-size:14px}.fl-f small{display:block;font-size:9px;color:var(--mu)}
.chat{flex:1;display:flex;flex-direction:column;min-width:0;overflow:hidden}
.ch-h{height:50px;border-bottom:1px solid var(--bd);display:flex;align-items:center;gap:10px;padding:0 14px}
.ch-h .nm{color:var(--bl);text-decoration:underline;font-weight:600}
.ch-h .av{width:34px;height:34px;font-size:13px}
.sel{border:1px solid var(--bd);border-radius:8px;padding:7px 10px;background:var(--sf);color:var(--tx);font:inherit;font-size:13px;width:140px}
.sim{font-size:12px;color:var(--g);border:1px dashed var(--g);border-radius:6px;padding:5px 9px;margin-left:auto}
.msgs{flex:1;overflow:auto;padding:16px 18px;display:flex;flex-direction:column;gap:16px}
.cm{align-self:flex-start;max-width:68%}.cm .who{display:flex;gap:8px;align-items:center;color:var(--mu);font-size:12px;margin-bottom:6px}.cm .who .av{width:24px;height:24px;font-size:10px}
.bb{background:var(--bub);padding:11px 14px;border-radius:10px;line-height:1.7;font-size:13px}
.cm time,.om time{display:block;font-size:11px;color:var(--mu);margin-top:4px}
.om{align-self:flex-end;max-width:70%}.om .who{text-align:right;font-size:11px;color:var(--mu);margin-bottom:4px}
.om .bb{background:var(--sf);border:1px solid var(--bd)}.om time{text-align:right}
.cp{padding:12px 16px;display:flex;gap:10px;align-items:center}
.cp .ib{border-radius:50%;width:40px;height:40px;color:var(--mu)}
.cp .in{flex:1;border:1px solid var(--bd);border-radius:22px;padding:0 14px;height:40px;display:flex;align-items:center;gap:8px;color:var(--mu)}
.cp input{flex:1;border:0;outline:0;background:none;font:inherit;font-size:13px;color:var(--tx)}
.aid{background:var(--gl);color:var(--gd);border-radius:99px;padding:5px 10px;font-size:12px;font-weight:700;display:flex;gap:4px;align-items:center;white-space:nowrap}
.rp{width:252px;flex-shrink:0;overflow:auto;padding:0 0 16px}
.rt{display:flex;justify-content:space-around;padding:12px 8px 8px;position:sticky;top:0;background:var(--sf);z-index:1}
.rt button{width:38px;height:38px;border-radius:8px;display:grid;place-items:center;color:var(--mu);position:relative}
.rt button.on{background:var(--gl);color:var(--g)}.rt button i{position:absolute;top:5px;right:5px;width:7px;height:7px;background:var(--g);border-radius:50%;animation:bl 1.6s infinite}
@keyframes bl{50%{opacity:.3}}
.pp{padding:8px 14px}.pp h3{font-size:14px;margin:6px 0 14px;display:flex;align-items:center;gap:8px}
.lb{display:inline-flex;align-items:center;gap:6px;background:var(--sf2);border-radius:6px;padding:5px 12px 5px 8px;font-size:12px}
.vl{padding:8px 4px 16px 10px;font-size:13px;line-height:1.6;word-break:break-all}.vl small{color:var(--mu);display:block}
.pe{margin-left:6px;color:var(--mu);vertical-align:middle}
.rm{height:100px;border-radius:6px;background:var(--sf2);display:grid;place-items:center;font-family:serif;color:#8a8a6a;letter-spacing:2px;margin:6px 4px}
.live{font-size:11px;color:var(--g);font-weight:600;margin-left:auto;display:flex;align-items:center;gap:4px}.live:before{content:"";width:6px;height:6px;border-radius:50%;background:var(--g);animation:bl 1.4s infinite}
.spin{display:none;color:var(--gd);font-size:12px;padding:6px 10px;background:var(--gl);border-radius:6px;margin-bottom:10px}.spin.on{display:block}
.aibox{background:var(--gl);border-radius:8px;padding:10px 12px;font-size:12.5px;line-height:1.7;margin:8px 0 16px}
.rec{border:1px solid var(--bd);border-radius:8px;padding:10px 12px;margin:8px 0;font-size:12.5px;line-height:1.6}.rec b{display:block;margin-bottom:3px}.rec button{color:var(--g);font-weight:700;margin-top:6px;font-size:12px}
.pp textarea{width:100%;height:150px;border:1px solid var(--bd);border-radius:8px;padding:10px;font:inherit;background:var(--sf2);color:var(--tx);resize:none}
.kv{display:flex;justify-content:space-between;padding:9px 0;border-bottom:1px solid var(--bd);font-size:12.5px;gap:8px}.kv span{color:var(--mu)}.kv b{font-weight:600;text-align:right}
/* modal */
.ov{position:fixed;inset:0;background:rgba(15,20,25,.55);display:none;align-items:center;justify-content:center;z-index:50;padding:24px}.ov.on{display:flex}
.modal{width:900px;max-width:100%;max-height:100%;overflow:auto;background:var(--sf);border-radius:16px;box-shadow:0 8px 30px rgba(0,0,0,.3)}
.mh{padding:18px 24px;border-bottom:1px solid var(--bd);display:flex;align-items:center;gap:14px;position:sticky;top:0;background:var(--sf);z-index:2}.mh .x{margin-left:auto;font-size:24px;color:var(--mu)}
.grid2{display:grid;grid-template-columns:1fr 1fr;gap:16px;padding:20px 24px}
.box{border:1px solid var(--bd);border-radius:12px;padding:16px}.box h3{margin:0 0 12px;font-size:14px}
.ir{display:flex;align-items:center;gap:10px;margin-bottom:10px;font-size:13px}.ir span:first-child{width:130px}.ir em{width:36px;text-align:right;font-style:normal;color:var(--mu)}
.tl{border-left:2px solid var(--bd);margin-left:6px;padding-left:16px}.tl div{position:relative;margin-bottom:12px;font-size:13px}.tl div:before{content:"";position:absolute;left:-23px;top:5px;width:10px;height:10px;border-radius:50%;background:var(--g);border:2px solid var(--sf)}.tl small{color:var(--mu);display:block}
.mf{padding:14px 24px;border-top:1px solid var(--bd);display:flex;gap:8px;justify-content:flex-end;align-items:center}.mf small{margin-right:auto;color:var(--mu)}
.toast{position:fixed;bottom:24px;left:50%;transform:translateX(-50%) translateY(20px);background:#222;color:#fff;padding:10px 18px;border-radius:10px;opacity:0;transition:.3s;z-index:99;pointer-events:none}.toast.on{opacity:1;transform:translateX(-50%)}
[hidden]{display:none!important}
</style>
</head>
<body>
<div class="app">
  <aside class="side"><div class="logo"><i>L</i>Message</div><div id="nav"></div></aside>
  <div class="main">
    <header class="top">
      <div class="acc"><span class="sa">c</span>couleur（クルール）<span class="ch" id="i-down"></span></div>
      <div class="ib" id="i-qr"></div>
      <div class="demo" id="demo"><button data-v="list" class="on">① 友だち一覧</button><button data-v="chat">② 個別トーク＆AI</button><button data-v="modal">③ AI分析レポート</button></div>
      <button class="up"><span id="i-sp1"></span>アップグレード</button>
      <div class="ti"><span id="i-msg2"></span>配信数</div><div class="ti"><span id="i-help"></span>サポート</div><div class="ti"><span id="i-bell"></span>お知らせ</div>
      <div class="th"><button class="ib" id="thb" title="画面テーマ"></button><div class="thm" id="thm" hidden></div></div>
      <div class="acc" style="width:170px"><span style="overflow:hidden;white-space:nowrap;text-overflow:ellipsis">オーガニック髪質改善サロン…</span></div>
    </header>

    <section class="view on" id="v-list">
      <div class="stats">
        <div class="card stat"><small>友だち総数</small><b>3,284</b></div>
        <div class="card stat"><small>AIプロファイル生成済み</small><b style="color:var(--g)">2,415</b></div>
        <div class="card stat"><small>来店意欲が高いお客様</small><b>268</b></div>
        <div class="card stat"><small>来店間隔が空いているお客様</small><b style="color:var(--wa)">142</b></div>
      </div>
      <div class="card">
        <div class="chips" id="chips"><button class="chip on" data-f="all">すべて</button><button class="chip" data-f="hot">来店意欲が高い</button><button class="chip" data-f="risk">来店間隔が空いている</button><button class="chip" data-f="new">新規</button><input class="s" id="q" placeholder="LINE名 / タグで検索"></div>
        <table><thead><tr><th>友だち</th><th>AI自動タグ</th><th>AIプロファイル概要</th><th>来店意欲</th><th></th></tr></thead><tbody id="tb"></tbody></table>
      </div>
    </section>

    <section class="view" id="v-chat">
      <div class="card fl">
        <div class="fl-t"><div class="dd">全ての友だち（非表示除く）<span id="i-chev"></span></div><div class="ib" id="i-fil"></div></div>
        <div class="fl-s"><span id="i-sr"></span><input id="fq" placeholder="LINE名 / システム表示名"></div>
        <div class="fl-b" id="fl"></div>
        <div class="fl-f"><span class="sa">c</span><div><small>送信ユーザー名</small>couleur（クルール）</div><span style="margin-left:auto;color:var(--mu)">⚙</span></div>
      </div>
      <div class="card chat">
        <div class="ch-h"><span id="i-bm" style="color:var(--mu)"></span><div class="av" id="cav"></div><span class="nm" id="cname"></span>
          <button class="sim" id="sim">デモ：お客様から返信が届く</button>
          <select class="sel" id="cst"><option>ステータスなし</option><option>未対応</option><option>対応中</option><option>対応済み</option></select></div>
        <div class="msgs" id="msgs"></div>
        <div class="cp"><div class="ib" id="i-clip"></div><div class="ib" id="i-mail"></div>
          <div class="in"><input id="inp" placeholder="メッセージを入力してください"><button class="aid" id="aidraft"><span id="i-sp2"></span>AI返信案</button><span id="i-smile"></span></div>
          <button id="send" style="color:var(--mu)"><span id="i-send"></span></button></div>
      </div>
      <div class="card rp">
        <div class="rt" id="rt"><button data-p="pb" title="基本情報"></button><button data-p="pf" title="友だち情報"></button><button data-p="pt" title="タグ"></button><button data-p="pm" title="メモ"></button><button class="on" data-p="pa" title="AIプロファイル"><i></i></button></div>
        <div id="pb" class="pp" hidden></div><div id="pf" class="pp" hidden></div><div id="pt" class="pp" hidden></div>
        <div id="pm" class="pp" hidden><h3>メモ</h3><textarea placeholder="施術メモ・カウンセリング内容を入力…"></textarea><button class="btn pri" style="margin-top:8px" id="memo">保存</button></div>
        <div id="pa" class="pp">
          <h3>AIプロファイル<span class="live">リアルタイム</span></h3><div class="spin" id="spin">AIがトーク内容を解析中…</div>
          <span class="lb"><span class="ic" data-i="sparkle" data-s="14"></span>AI要約</span><div class="aibox" id="psum"></div>
          <span class="lb"><span class="ic" data-i="chart" data-s="14"></span>来店意欲スコア</span><div class="vl row"><b id="pscore" style="font-size:20px;color:var(--g)"></b><div class="bar"><span id="pbar"></span></div></div>
          <span class="lb"><span class="ic" data-i="tag" data-s="14"></span>AI自動タグ</span><div class="vl" id="ptags"></div>
          <span class="lb"><span class="ic" data-i="msg" data-s="14"></span>おすすめアプローチ</span><div id="prec" style="padding:4px 0 10px"></div>
          <button class="btn pri" style="width:100%" id="rep">詳細な分析レポートを見る</button>
        </div>
      </div>
    </section>
  </div>
</div>

<div class="ov" id="ov"><div class="modal">
  <div class="mh"><div class="av" id="mav"></div><div><b id="mname" style="font-size:16px"></b><div style="color:var(--mu);font-size:12px">AI分析レポート｜couleur（クルール）｜分析精度 <b style="color:var(--g)">92%</b></div></div><button class="x" id="close">×</button></div>
  <div class="grid2">
    <div class="box"><h3>髪のお悩み・関心度</h3><div id="mint"></div></div>
    <div class="box"><h3>来店・購入傾向</h3><div id="mbuy"></div></div>
    <div class="box"><h3>行動タイムライン</h3><div class="tl" id="mtl"></div></div>
    <div class="box"><h3>AI推奨アクション</h3><div id="mact"></div></div>
  </div>
  <div class="mf"><small>※ トーク内容・リッチメニューの操作・予約履歴から自動生成しています</small><button class="btn" id="close2">閉じる</button><button class="btn pri" id="apply">AIタグを友だちに反映</button></div>
</div></div>
<div class="toast" id="toast"></div>

<script>
const $=s=>document.querySelector(s);
const P={msg:"M21 11.5a8.4 8.4 0 0 1-.9 3.8 8.5 8.5 0 0 1-7.6 4.7 8.4 8.4 0 0 1-3.8-.9L3 21l1.9-5.7a8.4 8.4 0 0 1-.9-3.8 8.5 8.5 0 0 1 4.7-7.6 8.4 8.4 0 0 1 3.8-.9h.5a8.5 8.5 0 0 1 8 8z",doc:"M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z M14 2v6h6 M16 13H8 M16 17H8",user:"M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2 M12 3a4 4 0 1 0 0 8 4 4 0 0 0 0-8z",tag:"M20.6 13.4l-7.2 7.2a2 2 0 0 1-2.8 0L2 12V2h10l8.6 8.6a2 2 0 0 1 0 2.8z M7 7h.01",db:"M12 2C7 2 3 3.5 3 5.5v13c0 2 4 3.5 9 3.5s9-1.5 9-3.5v-13C21 3.5 17 2 12 2z M3 5.5C3 7.5 7 9 12 9s9-1.5 9-3.5 M3 12c0 2 4 3.5 9 3.5s9-1.5 9-3.5",send:"M22 2L11 13 M22 2l-7 20-4-9-9-4z",clip:"M21.4 11l-9.2 9.2a6 6 0 0 1-8.5-8.5l9.2-9.2a4 4 0 0 1 5.7 5.7l-9.2 9.2a2 2 0 0 1-2.8-2.8l8.5-8.5",mail:"M4 4h16a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2z M22 6l-10 7L2 6",bm:"M19 21l-7-5-7 5V5a2 2 0 0 1 2-2h10a2 2 0 0 1 2 2z",edit:"M17 3a2.8 2.8 0 1 1 4 4L7.5 20.5 2 22l1.5-5.5z",sr:"M11 3a8 8 0 1 0 0 16 8 8 0 0 0 0-16z M21 21l-4.3-4.3",bell:"M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9 M13.7 21a2 2 0 0 1-3.4 0",list:"M8 6h13M8 12h13M8 18h13M3 6h.01M3 12h.01M3 18h.01",grid:"M3 3h7v7H3z M14 3h7v7h-7z M14 14h7v7h-7z M3 14h7v7H3z",cal:"M3 4h18v18H3z M16 2v4 M8 2v4 M3 10h18",box:"M21 8l-9-5-9 5v8l9 5 9-5z M3 8l9 5 9-5 M12 13v8",chart:"M18 20V10 M12 20V4 M6 20v-6",tool:"M14.7 6.3a4 4 0 0 0-5.4 5.4L3 18l3 3 6.3-6.3a4 4 0 0 0 5.4-5.4l-2.5 2.5-2.4-.6-.6-2.4z",chev:"M9 18l6-6-6-6",down:"M6 9l6 6 6-6",fil:"M4 6h16 M7 12h10 M10 18h4",smile:"M12 2a10 10 0 1 0 0 20 10 10 0 0 0 0-20z M8 14s1.5 2 4 2 4-2 4-2 M9 9h.01 M15 9h.01",help:"M12 2a10 10 0 1 0 0 20 10 10 0 0 0 0-20z M9.1 9a3 3 0 0 1 5.8 1c0 2-3 3-3 3 M12 17h.01",sparkle:"M12 3l1.9 5.1L19 10l-5.1 1.9L12 17l-1.9-5.1L5 10l5.1-1.9z M19 16v4 M17 18h4"};
const ic=(n,s=18)=>`<svg width="${s}" height="${s}" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="${P[n]}"/></svg>`;
const NAV=[["お気に入り"],["メッセージ関連"],["msg","1:1チャット",1,"chat"],["doc","テンプレート"],["msg","メッセージ配信"],["list","ステップ配信"],["user","あいさつメッセージ",1],["よく使われる機能"],["grid","リッチメニュー"],["doc","フォーム作成"],["bell","自動応答"],["grid","QRコードアクション"],["db","データ管理",1,"list"],["その他の機能"],["cal","予約管理",1],["box","商品販売"],["chart","データ分析",1],["tool","便利ツール",1]];
$("#nav").innerHTML=NAV.map(n=>n.length==1?`<div class="sl">${n[0]}</div>`:`<div class="nv" data-k="${n[3]||""}">${ic(n[0])}${n[1]}${n[2]?`<span class="ch">${ic("chev",14)}</span>`:""}</div>`).join("");
const ids={"i-down":["down",16],"i-qr":["grid",20],"i-sp1":["sparkle",16],"i-sp2":["sparkle",14],"i-msg2":["msg",20],"i-help":["help",20],"i-bell":["bell",20],"i-chev":["chev",14],"i-fil":["fil",18],"i-sr":["sr",15],"i-bm":["bm",18],"i-clip":["clip",18],"i-mail":["mail",18],"i-smile":["smile",18],"i-send":["send",22]};
for(const k in ids)$("#"+k).innerHTML=ic(...ids[k]);
document.querySelectorAll(".ic").forEach(e=>e.innerHTML=ic(e.dataset.i,+e.dataset.s));
document.querySelectorAll("#rt button").forEach((b,i)=>b.insertAdjacentHTML("afterbegin",ic(["db","user","tag","doc","sparkle"][i],19)));

const F=[
{id:1,n:"佐藤 美咲",c:"#e58fa8",st:"hot",score:86,date:"2026.10.20 21:14",src:"Instagram経由",menu:"【メイン】総合案内（予約・メニュー・紹介）",status:"対応中",unread:2,sty:"山田 さん",vis:"2回",hair:"うねり毛・敏感肌",
 tags:[["オーガニック志向"],["うねり・広がり改善に関心"],["定期便検討中"]],
 sum:"30代女性。梅雨以降の広がり・うねりに悩み、頭皮に優しい植物由来処方を重視。ホームケア定期便の料金を比較検討中で、来店予約の見込みが高い。",
 chat:[["他","はじめまして。敏感肌でも受けられるオーガニックの髪質改善トリートメントはありますか？","11/3 10:21"],["me","ご連絡ありがとうございます😊 当店は植物由来成分のみのオーガニック髪質改善をご用意しております。頭皮にも優しい処方です。","11/3 10:23"],["他","広がりとうねりがひどくて…ホームケアの定期便もあると聞きました。料金はどのくらいですか？","11/3 10:25"]],
 int:[["うねり・広がり改善",92],["オーガニック処方",85],["ホームケア定期便",70],["ヘッドスパ",38]],buy:[["想定単価","¥12,800"],["来店周期","2.5ヶ月"],["次回来店目安","11月中旬"],["価格感度","低（品質重視）"],["響く訴求","成分・施術事例"]],
 tl:[["今日 10:25","定期便の料金について質問"],["昨日","リッチメニュー「Menu」を3回タップ"],["11/1","髪質改善トリートメントを初回体験"],["10/20","友だち追加（Instagram経由）"]],
 rec:[["定期便の特典をご案内","「初回15%OFF・いつでも休止OK」とお伝えし、価格面の不安を解消しましょう。","ホームケア定期便は初回15%OFFで、休止・解約もいつでも可能です🌿 植物由来成分なので敏感肌の方にも安心です。"],["施術ビフォーアフターを送付","うねり・広がり改善の事例が来店の後押しになります。","同じお悩みのお客様のビフォーアフターをお送りしますね。次回のご予約もお取りできます✨"]],
 sim:["あと、施術時間はどのくらいですか？ 平日の夜でも予約できますか？",["平日夜の来店希望"]]},
{id:2,n:"田中 彩花",c:"#7aa7d9",st:"risk",score:41,date:"2026.06.02 12:40",src:"店舗QRコード",menu:"【リピーター】次回予約のご案内",status:"未対応",unread:0,sty:"佐々木 さん",vis:"5回",hair:"ブリーチ毛・ダメージ",
 tags:[["ダメージ毛ケア"],["ブリーチ履歴あり"],["来店間隔が空いている","w"]],
 sum:"40代女性。ブリーチ後のダメージ補修で定期的に来店していたが、直近4ヶ月は来店がなくメッセージ開封率も低下。再来店のきっかけづくりが必要。",
 chat:[["他","前回のトリートメント、持ちがイマイチだった気がして…","昨日 18:02"],["me","ご不安にさせてしまい申し訳ありません。髪の状態を確認させてください。","昨日 18:30"]],
 int:[["ダメージ補修",88],["カラーの色持ち",64],["ホームケア",30]],buy:[["想定単価","¥15,400"],["来店周期","2ヶ月→4ヶ月超"],["次回来店目安","要フォロー"],["価格感度","中"],["響く訴求","保証・再施術"]],
 tl:[["昨日","施術後の持ちについて不満を送信"],["10/15","配信メッセージの未開封が続く"],["7/8","オーガニックカラー＋トリートメント"]],
 rec:[["不安に寄り添うフォローを優先","まず状況確認と再施術のご案内を。信頼回復が最優先です。","持ちの件、再度髪の状態を見て最適なケアをご提案させてください。お時間のよい日をお知らせください。"],["再来店クーポンの案内","来店間隔が空いているため、限定クーポンで背中を押します。","ご不便のお詫びに、次回ご来店時のトリートメント10%OFFをお贈りします🎁"]],
 sim:["前回のカラーが色落ちしてきたので、また相談したいです。",["色落ち相談"]]},
{id:3,n:"鈴木 あかり",c:"#f0a35e",st:"new",score:58,date:"2026.11.02 09:15",src:"通常友だち追加",menu:"【新規】初回限定クーポン案内",status:"未対応",unread:1,sty:"未設定",vis:"0回",hair:"細毛・軟毛",
 tags:[["新規"],["初回クーポン使用予定"],["時短ケア重視"]],
 sum:"20代女性。今週友だち追加。初回クーポンを確認済みで、忙しくても続けやすい時短ケアに関心。来店日の確定が次のステップ。",
 chat:[["他","初回クーポンは土日でも使えますか？","11/4 09:02"]],
 int:[["時短・手軽さ",80],["ボリュームUP",66],["オーガニック処方",52]],buy:[["想定単価","¥8,800"],["来店周期","—（未来店）"],["次回来店目安","今週末希望"],["価格感度","中"],["響く訴求","初回特典・口コミ"]],
 tl:[["今日 09:02","クーポンの利用条件を質問"],["昨日","リッチメニュー「Menu」をタップ"],["11/2","友だち追加"]],
 rec:[["土日の空き枠をご案内","利用条件を明確に伝え、来店日を確定させましょう。","土日もご利用いただけます！今週末の空き状況をお送りしますね🌿"]],
 sim:["じゃあ土曜の午前に行きたいです。時間はどのくらいかかりますか？",["土曜午前を希望"]]},
{id:4,n:"高橋 結衣",c:"#6fbf9a",st:"hot",score:91,date:"2025.03.11 15:30",src:"友人紹介",menu:"【VIP】ヘッドスパ会員のご案内",status:"対応済み",unread:0,sty:"山田 さん",vis:"14回",hair:"普通毛・頭皮ケア",
 tags:[["ヘッドスパ愛用"],["店販購入が多い"],["常連（紹介実績あり）"]],
 sum:"30代女性。ヘッドスパ愛用の常連で、店販シャンプーも継続購入。紹介実績あり。コース延長やVIP向け施策の反応が期待できる。",
 chat:[["他","来月のヘッドスパ、コースを延長したいです！","昨日 20:11"],["me","ありがとうございます！延長コースの空きを確認いたします。","昨日 20:15"]],
 int:[["ヘッドスパ",95],["店販ホームケア",78],["オーガニック処方",74]],buy:[["想定単価","¥21,000"],["来店周期","1.2ヶ月"],["次回来店目安","12月上旬"],["価格感度","低"],["響く訴求","限定・先行案内"]],
 tl:[["昨日","ヘッドスパ延長の相談"],["11/2","店販ページを5回閲覧"],["10/10","髪質改善＋ヘッドスパ ¥24,800"]],
 rec:[["VIP会員の先行予約を案内","常連のお客様には先行枠のご案内が高効果です。","来月のヘッドスパ延長コース、VIP枠で先行予約を承っております✨"]],
 sim:["友だちも連れて行っていいですか？ 紹介特典も気になります。",["紹介特典に関心"]]}
];
let cur=F[0],filt="all",pend=null;
const tg=(t,c="")=>`<span class="tag ${t[1]||""} ${c}">${t[0]}</span>`;
const av=(f,e)=>{e.style.background=f.c;e.textContent=f.n[0]};
const now=()=>{const d=new Date();return "今日 "+d.getHours()+":"+String(d.getMinutes()).padStart(2,"0")};
const toast=t=>{const e=$("#toast");e.textContent=t;e.classList.add("on");setTimeout(()=>e.classList.remove("on"),2200)};

function renderList(){const q=$("#q").value.trim();
 $("#tb").innerHTML=F.filter(f=>(filt=="all"||f.st==filt)&&(!q||(f.n+f.tags.map(t=>t[0]).join()).includes(q))).map(f=>`<tr class="fr" data-id="${f.id}"><td><div class="row"><div class="av" style="background:${f.c}">${f.n[0]}</div><b>${f.n}</b></div></td><td>${f.tags.map(t=>tg(t)).join("")}</td><td><div class="sum">${f.sum}</div></td><td style="width:150px"><div class="score">${f.score}<div class="bar"><span style="width:${f.score}%;background:${f.score>70?"var(--g)":f.score>50?"var(--wa)":"var(--rd)"}"></span></div></div></td><td><button class="btn">トークを開く</button></td></tr>`).join("")}
function renderFL(){const q=$("#fq").value.trim();
 $("#fl").innerHTML=F.filter(f=>!q||f.n.includes(q)).map(f=>{const l=f.chat[f.chat.length-1];return `<div class="fi ${f.id==cur.id?"on":""}" data-id="${f.id}"><div class="av" style="background:${f.c}">${f.n[0]}</div><div class="mid"><b>${f.n}</b><div class="pv">${l[1]}</div></div><span class="tm">${l[2].split(" ")[0]}</span>${f.unread?`<span class="ub">${f.unread}</span>`:""}</div>`}).join("")}
function renderBasic(){const r=(i,l,v,e)=>`<span class="lb">${ic(i,14)}${l}</span>${e?`<span class="pe">${ic("edit",13)}</span>`:""}<div class="vl">${v}</div>`;
 $("#pb").innerHTML=`<h3>基本情報</h3>`+r("user","LINE名",`${cur.n}<small>${cur.date} 既存友だち</small>`)+r("user","システム表示名","-",1)+r("user","流入経路",cur.src)+r("list","ステップ配信","配信中のステップなし",1)+r("grid","リッチメニュー",cur.menu,1)+`<div class="rm">couleur</div>`;
 $("#pf").innerHTML=`<h3>友だち情報</h3>`+[["髪質・お悩み",cur.hair],["担当スタイリスト",cur.sty],["来店回数",cur.vis],["アレルギー","なし"],["次回予約","未予約"]].map(k=>`<div class="kv"><span>${k[0]}</span><b>${k[1]}</b></div>`).join("");
 $("#pt").innerHTML=`<h3>タグ</h3>${cur.tags.map(t=>tg(t,"")).join("")}<div style="font-size:11px;color:var(--mu);margin-top:10px">※ AIプロファイルから自動付与されたタグを含みます</div>`}
function renderPanel(){$("#psum").textContent=cur.sum;$("#pscore").textContent=cur.score;$("#pbar").style.width=cur.score+"%";
 $("#ptags").innerHTML=cur.tags.map(t=>tg(t)).join("");
 $("#prec").innerHTML=cur.rec.map((r,i)=>`<div class="rec"><b>${r[0]}</b>${r[1]}<br><button data-i="${i}">返信案を入力欄に挿入 →</button></div>`).join("")}
function renderChat(){cur.unread=0;renderFL();renderBasic();renderPanel();av(cur,$("#cav"));$("#cname").textContent=cur.n;$("#cst").value=cur.status;
 $("#msgs").innerHTML=cur.chat.map(m=>m[0]=="me"?`<div class="om"><div class="who">アクション送信　couleur（クルール）</div><div class="bb">${m[1]}</div><time>${m[2]}</time></div>`:`<div class="cm"><div class="who"><div class="av" style="background:${cur.c}">${cur.n[0]}</div>${cur.n}</div><div class="bb">${m[1]}</div><time>${m[2]}</time></div>`).join("");$("#msgs").scrollTop=1e5}
function renderModal(){av(cur,$("#mav"));$("#mname").textContent=cur.n+" さん";
 $("#mint").innerHTML=cur.int.map(i=>`<div class="ir"><span>${i[0]}</span><div class="bar"><span style="width:${i[1]}%"></span></div><em>${i[1]}%</em></div>`).join("");
 $("#mbuy").innerHTML=cur.buy.map(b=>`<div class="kv"><span>${b[0]}</span><b>${b[1]}</b></div>`).join("")+`<div class="aibox">${cur.sum}</div>`;
 $("#mtl").innerHTML=cur.tl.map(t=>`<div><small>${t[0]}</small>${t[1]}</div>`).join("");
 $("#mact").innerHTML=cur.rec.map(r=>`<div class="rec"><b>${r[0]}</b>${r[1]}</div>`).join("")}

let last="list";
function go(v){document.querySelectorAll("#demo button").forEach(b=>b.classList.toggle("on",b.dataset.v==v));
 if(v=="modal"){if(last=="list")show("chat");renderModal();$("#ov").classList.add("on")}else{$("#ov").classList.remove("on");show(v);last=v}}
function show(v){document.querySelectorAll(".view").forEach(e=>e.classList.remove("on"));$("#v-"+v).classList.add("on");
 document.querySelectorAll(".nv").forEach(n=>n.classList.toggle("on",n.dataset.k==v));if(v=="chat")renderChat()}
function analyze(cb){$("#spin").classList.add("on");setTimeout(()=>{$("#spin").classList.remove("on");cb()},1200)}

$("#demo").onclick=e=>{const b=e.target.closest("button");if(b)go(b.dataset.v)};
$("#nav").onclick=e=>{const n=e.target.closest(".nv");if(n&&n.dataset.k)go(n.dataset.k)};
$("#chips").onclick=e=>{const b=e.target.closest(".chip");if(!b)return;filt=b.dataset.f;document.querySelectorAll(".chip").forEach(c=>c.classList.toggle("on",c==b));renderList()};
$("#q").oninput=renderList;$("#fq").oninput=renderFL;
$("#tb").onclick=e=>{const r=e.target.closest("tr");if(r){cur=F.find(f=>f.id==r.dataset.id);go("chat")}};
$("#fl").onclick=e=>{const r=e.target.closest(".fi");if(r){cur=F.find(f=>f.id==r.dataset.id);renderChat()}};
$("#cst").onchange=e=>{cur.status=e.target.value;toast("ステータスを「"+cur.status+"」に変更しました")};
$("#rt").onclick=e=>{const b=e.target.closest("button");if(!b)return;document.querySelectorAll("#rt button").forEach(x=>x.classList.toggle("on",x==b));["pb","pf","pt","pm","pa"].forEach(i=>$("#"+i).hidden=i!=b.dataset.p)};
$("#prec").onclick=e=>{const b=e.target.closest("button");if(b){$("#inp").value=cur.rec[b.dataset.i][2];$("#inp").focus()}};
$("#aidraft").onclick=()=>{const t=cur.rec[0][2];let i=0;$("#inp").value="";const iv=setInterval(()=>{$("#inp").value=t.slice(0,++i);if(i>=t.length)clearInterval(iv)},22)};
const send=()=>{const v=$("#inp").value.trim();if(!v)return;cur.chat.push(["me",v,now()]);$("#inp").value="";renderChat()};
$("#send").onclick=send;$("#inp").onkeydown=e=>{if(e.key=="Enter"&&!e.isComposing)send()};
$("#sim").onclick=()=>{cur.chat.push(["他",cur.sim[0],now()]);renderChat();$("#rt [data-p=pa]").click();
 analyze(()=>{cur.score=Math.min(99,cur.score+4);cur.tags.push(cur.sim[1]);renderPanel();renderBasic();$("#ptags").lastChild.classList.add("new");toast("AIが新しいタグ「"+cur.sim[1][0]+"」を追加しました")})};
$("#rep").onclick=()=>go("modal");
$("#close").onclick=$("#close2").onclick=()=>go("chat");$("#ov").onclick=e=>{if(e.target.id=="ov")go("chat")};
$("#apply").onclick=()=>{toast("AIタグを友だち情報に反映しました ✓");go("chat")};
$("#memo").onclick=()=>toast("メモを保存しました");
/* ===== テーマ切り替え ===== */
P.palette="M12 2a10 10 0 1 0 0 20c1.1 0 2-.9 2-2 0-.5-.2-1-.5-1.3-.3-.3-.5-.8-.5-1.3 0-1.1.9-2 2-2H17a5 5 0 0 0 5-5c0-4.9-4.5-8.4-10-8.4z M7.5 11h.01 M12 7h.01 M16.5 11h.01";
$("#thb").innerHTML=ic("palette",20);
const TH=[["light","標準（エルメライト）","清潔感のある白背景","#ffffff","#08bf5a"],["dark","ダークモード","目が疲れにくい黒・ダークグレー","#1e1e1e","#10c96a"],["sage","オーガニックセージ","淡いグリーンの自然な基調","#e8eee3","#5f8f5a"],["lavender","ラベンダーロゼ","淡いピンク・パープルでリラックス","#f4edf7","#a35fc0"]];
let theme="light";
function applyTheme(t,notify){theme=t;document.documentElement.dataset.theme=t;try{localStorage.setItem("lm-theme",t)}catch(e){}
 $("#thm").innerHTML=`<h4>画面カラーテーマ</h4>`+TH.map(x=>`<button class="to ${x[0]==t?"on":""}" data-t="${x[0]}"><span class="sw" style="background:linear-gradient(135deg,${x[3]} 50%,${x[4]} 50%)"></span><span>${x[1]}<small>${x[2]}</small></span>${x[0]==t?'<span class="ck">✓</span>':""}</button>`).join("");
 if(notify)toast("テーマを「"+TH.find(x=>x[0]==t)[1]+"」に変更しました")}
$("#thb").onclick=e=>{e.stopPropagation();$("#thm").hidden=!$("#thm").hidden};
$("#thm").onclick=e=>{e.stopPropagation();const b=e.target.closest(".to");if(b){applyTheme(b.dataset.t,true);$("#thm").hidden=false}};
document.addEventListener("click",()=>$("#thm").hidden=true);
let saved="light";try{saved=localStorage.getItem("lm-theme")||"light"}catch(e){}
applyTheme(TH.some(x=>x[0]==saved)?saved:"light");
renderList();show("list");
</script>
</body>
</html>
