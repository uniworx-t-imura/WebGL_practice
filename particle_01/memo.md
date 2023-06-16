# Particle memo
https://liginc.co.jp/548806

## 円の書き出し
class Particle {
  constructor(x, y, radius, directionX, directionY) {
    this.x = x;
    this.y = y;
    this.radius = radius;
    this.directionX = directionX;
    this.directionY = directionY;
  }
  render() {
    // 円をかく
    ctx.beginPath();
    ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2, true);
    ctx.fillStyle = "#E67A7A";
    ctx.fill();
  }
}

const particle = new Particle(100, 100, 10, 0, 0);
particle.render();



## window.requestAnimationFrame() メソッド
https://developer.mozilla.org/ja/docs/Web/API/Window/requestAnimationFrame

## setTimeout() との違いや経過時間の取得ほか
https://www.webdesignleaves.com/pr/jquery/requestAnimationFrame.html

## requestAnimationFrame() メソッドについて
呼び出しは1回のみ実行されるので、アニメーションなどの処理を継続的に要求するためには、ある種のループを作成して繰り返し処理をする必要がある。
基本的には、requestAnimationFrame() に指定するコールバック関数を定義して、そのコールバック関数の中で requestAnimationFrame() を使って自身を呼び出し、ブラウザの描画のタイミングに合わせてコールバック関数を繰り返し実行（ループ）させる。


