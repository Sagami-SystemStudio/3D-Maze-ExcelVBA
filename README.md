# 3D MAZE ExcelVBA
Development using Excel VBA

## 3D Maze 仕様
1. マップ表示はオートシェイプを使用します
2. 全体マップと3D表示マップを実装しました  
  全体マップ：20×20の全体マップです (スタートとゴールに●を表示します)  
  3Dマップ：縦8階層×横9ブロックの3D表示の元データです  
3. 3Dマップは常にユーザの正面目線で描画しています  
  全体マップで北向きのとき：ユーザの現在位置の上側を描画  
  全体マップで東向きのとき：ユーザの現在位置の右側を描画  
  全体マップで南向きのとき：ユーザの現在位置の下側を描画  
  全体マップで西向きのとき：ユーザの現在位置の左側を描画  
4. コマンドボタンは「前進む」「左向く」「右向く」を実装しました
5. 3D表示エリアは64セル×64セルです
6. 前回の３Dマップ描画で壁が足りなかった部分を修正しました  
  四角形と台形の表示処理  
  6-1.) 壁（情報コード=9、99）のときの3D描画  
  ・描画対象外（目に見えない範囲 情報コード=7、8）ならスキップ  
  ・手前の壁（四角形）を描画する  
  6-2.) 通路（情報コード=1、2、0）のときの3D描画  
  ・中央より左（0から3）のとき、左が壁なら左側に台形を描画  
  ・中央より右（5から7）のとき、右が壁なら右側に台形を描画  
  ・中央（4）のとき左が壁なら左側、右が壁なら右側、両方なら両方に台形を描画  
  6-3.) 通路のとき前のブロックが壁なら前面に四角形を描画  

## 開発環境
Microsoft Office 2016

## 使い方
適当なところにソースを貼り付けてください
シート初期化() を実行すると3D迷路を描画します
※アクティブセルの情報を全てクリアしますのでご注意ください

## バグ報告
本ソフトにつきましてのご感想・ご意見・バグ報告などは作者までお伝えいただけると幸いです。
バグ修正、要望などできる限り応えたいと思います

## ライセンス(license)
パブリックドメイン(public domain)

## 掲載ブログ
<http://pg-sample.sagami-ss.net/?eid=54>
