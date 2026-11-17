# プライバシーポリシー / Privacy Policy

最終更新: 2026-10-06

fitbit-health（以下「本アプリ」）は、作成者本人が自分の健康データを取得するための個人用ツールです。
作成者本人以外は使用しません。

## 取得するデータ

Google Health API から、作成者本人のアカウントについて、次のデータを **読み取り専用** で取得します。

- 睡眠（時刻、睡眠時間、睡眠ステージごとの時間）
- 歩数
- 心拍、安静時心拍、血中酸素（SpO2）、心拍変動（HRV）、呼吸数、体重などの健康指標

## 利用目的

作成者本人が、自分の健康データを確認し、自分のプログラム（音声で知らせるデバイスなど）で活用するためだけに使います。

## 保存と管理

- 取得したデータは、作成者本人が管理する環境にだけ保存します。
  - 作成者のパソコン上のファイル
  - 作成者が管理する Cloudflare Workers KV（睡眠・歩数などの集計値。日々上書きされ、古い値は残りません）
- OAuth の認証情報（Client Secret、Refresh Token）は、ソースコードに含めず、環境変数または暗号化されたシークレットとして管理します。
- 音声での応答文を作るために、睡眠時間や歩数などの要約した値を、作成者が選んだ生成 AI サービスに送ることがあります。

## 第三者への提供

取得したデータを、第三者に販売、提供、公開することはありません。広告にも利用しません。

## Google API Services User Data Policy

本アプリによる Google から受け取った情報の使用と他のアプリへの転送は、
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy)
（Limited Use の要件を含む）に準拠します。

## アクセス権の取り消しとデータの削除

作成者は、いつでも <https://myaccount.google.com/permissions> から本アプリのアクセス権を取り消せます。
保存したデータは、作成者自身がいつでも削除できます。

## 連絡先

hfujikawa77@gmail.com

---

## Summary (English)

fitbit-health is a personal-use tool by its author. It reads the author's own sleep, steps, and health metrics from the
Google Health API (read-only) and stores them only in environments the author controls. The data is not sold, shared with
third parties, or used for advertising. Use of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.
