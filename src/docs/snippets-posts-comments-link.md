<!--
@@@title:Posts comments link@@@
@@@section:Snippets@@@
-->

# Posts comments link

Link to the comments on the post.

##### Usage

```html
<b:loop values='data:posts' var='post'>
  ...
</b:loop>
```


## Default

```html
<b:if cond='data:post.allowComments'>
  <a b:whitespace='remove' expr:href='data:post.commentsUrl' expr:title='data:messages.comments'>
    <b:if cond='data:post.commentSource != 1'>
      <b:message name='messages.numberOfComments'>
        <b:param expr:value='data:post.numberOfComments' name='numComments'/>
      </b:message>
    <b:else/><!-- fallback -->
      <span><data:messages.comments/></span>
    </b:if>
  </a>
</b:if>
```
