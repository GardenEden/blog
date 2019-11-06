---
layout: comments
title: 留言
---
交换友链可以在评论区留言~

- [w_weilan](https://blog.csdn.net/w_weilan)：旧的CSDN博客
- [刻苦驴啊](https://blog.csdn.net/D5__J9)：大哥+舍友，很耐心的解决我很多问题~
- [shadw3002](https://shadw3002.github.io)：同学+基友，常在一起交流技♂术
- [水唐](https://yorkking.github.io)：同学+基友，热爱数学（自称为“紧跟大佬的菜鸡挣扎者”
- [Ender](https://ender-coder.github.io)：可♂爱的学弟

{% if site.gitment_repo %}
<div id="gitmentContainer"></div>
<link rel="stylesheet" href="https://imsun.github.io/gitment/style/default.css">
<script src="https://imsun.github.io/gitment/dist/gitment.browser.js"></script>
<script>
    var gitment = new Gitment({
        id: '<%= page.date %>',
        owner: '{{site.github_username}}',
        repo: '{{site.gitment_repo}}',
        oauth: {
            client_id: '{{site.gitment_clientId}}',
            client_secret: '{{site.gitment_clientSecret}}',
        },
    });
    gitment.render('gitmentContainer')
</script>
{% endif %}