---
rank: 4
related_endpoints: []
related_resources: []
related_guides:
  - authentication/select
required_guides:
  - applications/select
alias_paths:
  - /docs/authenticate-with-developer-token
category_id: authentication
subcategory_id: authentication/access-tokens
id: authentication/access-tokens/developer-tokens
type: guide
is_index: false
total_steps: 8
sibling_id: authentication/access-tokens
parent_id: authentication/access-tokens
next_page_id: authentication/access-tokens/refresh
previous_page_id: authentication/access-tokens/sdks
---
# Developerトークン

Developerトークンは、開発およびテスト中に開発者が利用できるアクセストークンです。これらのトークンは60分後に期限切れになる有効期間の短いトークンで、自動で更新することはできません。

Developerトークンは、**常に開発者のユーザーアカウントとして認証**され、その他のユーザーとして認証されることはありません。この点が、他の大半の認証方式と異なります。

## Developerトークンの作成

アプリケーション用にDeveloperトークンを作成するには:

* Box[開発者コンソール][devconsole]に移動し、Developerトークンの作成対象となるアプリケーションを選択します。
* サイドバーで\[構成]を選択します。
* \[Developerトークン]セクションで、\[Developerトークンを生成]を選択します。

## Developerトークンの使用

Developerトークンは、さまざまなアクセストークンと同様、API呼び出しの`Authorization`ヘッダーで使用できます。

```curl
curl https://api.box.com/2.0/users/me \
  -H "Authorization: Bearer [DEVELOPER_TOKEN]"
```

<Message warning>

Developerトークンは、トークン作成時に開発者コンソールにログインしていたユーザー(開発者)に関連付けられていることに注意してください。

</Message>

SDKのほとんどは、基本のAPIクライアントを作成する際に、Developerトークンを使用して初期化することもできます。

<Samples id="x_auth" variant="init_with_dev_token">

</Samples>

<Message type="danger">

# Developerトークンは実稼働環境で使用しないでください

Developerトークンは、開発およびテストのためだけに使用してください。トークンは自動的に有効期限が切れても、自動更新できないため、実稼働環境での効果は限定的です。

</Message>

[devconsole]: https://app.box.com/developers/console
