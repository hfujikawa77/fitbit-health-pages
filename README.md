# fitbit-health

作成者本人が、自分の Fitbit の健康データ（睡眠・歩数など）を、自分のプログラムから取得するための個人用ツールです。
一般公開はしておらず、作成者本人以外は使用しません。

An OAuth client for personal use only. It reads the author's own Fitbit data (sleep, steps, and similar health metrics)
through the Google Health API. It is not distributed to other users.

## 何をするか

- Google Health API から、作成者自身の睡眠・歩数・心拍などの健康指標を **読み取り専用** で取得します。
- 取得した値を、作成者自身が管理する環境（ローカルのファイルと、Cloudflare Workers KV）に保存します。
- 要求するスコープ（すべて読み取り専用）:
  - `https://www.googleapis.com/auth/googlehealth.sleep.readonly`
  - `https://www.googleapis.com/auth/googlehealth.activity_and_fitness.readonly`
  - `https://www.googleapis.com/auth/googlehealth.health_metrics_and_measurements.readonly`
- データの書き込み・削除は行いません。

## 関連

- [プライバシーポリシー](./PRIVACY.md)

## 連絡先

hfujikawa77@gmail.com
