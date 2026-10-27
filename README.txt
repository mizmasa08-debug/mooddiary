MoodDiary iPhone向け PWA（Android版とは別アプリ）

■ ファイルの公開（GitHub Pages）
1. GitHubの無料アカウントを作成。
2. 新しい公開リポジトリ（例：mooddiary-pwa）を作成。
3. このフォルダ内の7ファイル（index.html, style.css, app.js, sw.js, manifest.webmanifest, icon-192.png, icon-512.png）をリポジトリの一番上の階層にアップロードしてCommit。
4. リポジトリの Settings → Pages → Build and deployment で「Deploy from a branch」を選択、Branch「main」、Folder「/(root)」でSave。
5. 表示された https://ユーザー名.github.io/mooddiary-pwa/ をSafariで開く。
6. Safariの共有メニュー →「ホーム画面に追加」→「追加」。

■ 仕様
記録はブラウザーの端末内（localStorage）へ保存し、サーバー側にはアップロードしません。
JSONのformat:mooddiary-backup、version:1、entries配列はAndroid版と同じです。
バックアップを取り、復元で取り込めます。取り込みは「置換」であり追記ではありません。
カレンダーは年月指定、前月・翌月移動、左右スワイプが可能です。
グラフは0/25/50/75/100の縦軸、期間7/30/90日/全期間に対応します。

■ 注意
GitHub Pages上のソースコードは公開されます。記録データそのものはアップロードしません。
Safariのデータ消去、端末変更などでデータを失う可能性があります。定期的にJSONでバックアップしてください。
公開後はHTTPSで実際のiPhone動作確認が必要です。
このフォルダの構成はローカル環境での静的チェックのみ実施。iPhone実機テストは未実施です。
