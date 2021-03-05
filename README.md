# Link to project: https://component-reuse.vercel.app/

<img width="479" alt="Screen Shot 2021-03-05 at 5 14 14 PM" src="https://user-images.githubusercontent.com/3590386/110123113-13f0b880-7df3-11eb-90c0-2f3563ca5d49.png">

```JSX
<div className="ui card">
  <div className="content">{children}</div>
  <div className="extra content">
    <div className="ui two buttons">
      <div className="ui basic green button">Approve</div>
      <div className="ui basic red button">Reject</div>
    </div>
  </div>
</div>
```

The `<ApprovalCard` component can reused to render different child elements such as a regular `<div>` or a `CommentDetail` component.

```JSX
<ApprovalCard>
  <div>
    <h4>Warning</h4>
    Are you sure you want to do this?
  </div>
</ApprovalCard>
```

```JSX
<ApprovalCard>
  <CommentDetail
    author="Sam"
    timeAgo="Today at 4:45PM"
    content="Nice blog post"
    avatar={faker.image.image()} />
</ApprovalCard>
```
