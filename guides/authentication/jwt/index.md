---
rank: 2
related_endpoints: []
related_guides:
  - applications/select
  - authentication/user-types
  - authentication/select
required_guides:
  - authentication/select
related_resources: []
alias_paths:
  - /docs/authenticate-with-jwt
  - /docs/app-auth
category_id: authentication
subcategory_id: authentication/jwt
id: authentication/jwt
type: guide
is_index: true
total_steps: 4
sibling_id: authentication
parent_id: authentication
next_page_id: authentication/jwt/as-user
previous_page_id: authentication/jwt/with-sdk
---
# JWT認証

JWTを使用するサーバー側の認証は、Box APIで認証するための最も強力な方法の1つです。JWTは、効果的にサーバー間認証を実現するよう設計された[オープンスタンダード](https://jwt.io/)です。

<ImageFrame border>

![JWTフロー](./jwt-flow.png)

</ImageFrame>

JSON Web Token (JWT)を使用するサーバー側の認証は、カスタムアプリと企業統合のみで使用できます。ユーザーが承認フローに関与することはないため、社内の任意のユーザーの代わりに処理を実行するために使用できます。JWTでは、公開/秘密キーペアを使用してアプリケーションの権限を確認します。

## JWTの制限

Server-side authentication using JWT works by creating a claim on the
application's server and then signing this using the application's secret key.
In most cases, the claim is that the server is allowed to act on
behalf of the Box application.

For this reason every application that uses JWT has an associated [Service
Account](g://authentication/user-types) that is the default user that it
authenticates as. This user is an admin-like user and for this
reason JWT applications require an actual Box admin's approval before they can
be used.

## JWTを使用する場合

JWTを使用するサーバー側認証は、以下に当てはまるアプリに最適な認証方式です。

* Boxアカウントを持たないユーザーを使用する
* 独自のIDシステムを使用する
* ユーザーにBoxを使用していることを認識させたくない
* アプリケーションのBoxアカウントにデータを保存し、ユーザーのBoxアカウントには保存しない
