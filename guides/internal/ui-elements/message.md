---
hide: true
category_id: internal
subcategory_id: internal/ui-elements
id: internal/ui-elements/message
type: guide
is_index: false
rank: 0
total_steps: 8
sibling_id: internal/ui-elements
parent_id: internal/ui-elements
next_page_id: internal/ui-elements
previous_page_id: ''
---
<!-- does not need translation -->

# Message

A message is a way to show a user that something is worth noting.

## Message types

### デフォルトのメッセージ

The lowest level of message is default message. Either explicitly set the type, or
omit the type. Use this message type for messages that are not essential to be read.

```html
<Message>
  A default note
</Message>

<default type='default'>
  A default note
</Message>
```

<H>

<Message>

デフォルトのメモ

</Message>

</H>

## 通知メッセージ

The next level is a notice. Use this message type for messages that are notices
but would not break anything for the user if ignored.

```html
<Message type='notice'>
  A notice message
</Message>

<Message notice>
  A notice message
</Message>
```

<H>

<Message Notice>

通知メッセージ

</Message>

</H>

## 警告メッセージ

The next level of message is a warning. Use this message type for messages that
are notices that might cause an error or exception for the user if ignored, or
to point out that an error or exception might occur when they complete the
action previously described.

```html
<Message type='warning'>
  A warning note
</Message>

<Message warning>
  A warning note
</Message>
```

<H>

<Message warning>

警告メモ

</Message>

</H>

## 危険メッセージ

The final level of message is a danger warning. Use this message type for
messages that are notices that can be attached to actions that will likely cause
an error or exception for the user.

```html
<Message type='danger'>
  Danger zone!
</Message>

<Message danger>
  Danger zone!
</Message>
```

<H>

<Message danger>

危険なゾーン

</Message>

</H>

## タイトル

A message can have a title. Please only use `<h1>` titles.

```html
<Message>
  # A title

  A default note
</Message>
```

<H>

<Message>

# タイトル

デフォルトのメモ

</Message>

</H>

## Size

A message can be made smaller than the default.

```html
<Message size='small'>
  A small note
</Message>
```

<H>

<Message size="small">

A small note

</Message>

</H>
