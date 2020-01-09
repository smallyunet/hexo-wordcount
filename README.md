# A fork from Hexo-WordCount

## Installation

```bash
yarn add hexo-wordcount-sy
# or
npm i --save hexo-wordcount-sy
```

## Usage

### 字数统计 WordCount

```js
wordcount(post.content)
```

### 阅读时长预计 Min2Read

```js
min2read(post.content)
```

设置阅读速度 Set Reading Speed:

```js
min2read(post.content, {cn: 300, en: 160})
```

### 总字数统计 TotalCount

```js
totalcount(site)        // 12345
totalcount(site, 'k')   // 12.3k
totalcount(site, ',')   // 12,345
```

## Demo

### Swig

Post Count:

```swig
   <span class="post-count">{{ wordcount(post.content) }}</span>
```

Post Minutes to Read:

```swig
   <span class="post-count">{{ min2read(post.content) }}</span>
```

Total Count:

```swig
   <span class="post-count">{{ totalcount(site) }}</span>
```

### Ejs

Post Count:

```ejs
   <span class="post-count"><%= wordcount(post.content) %></span>
```

Post Minutes to Read:

```ejs
   <span class="post-count"><%= min2read(post.content) %></span>
```

Total Count:

```ejs
   <span class="post-count"><%= totalcount(site) %></span>
```

### Jade

Post Count:

```jade
   span.post-count= wordcount(post.content)
```

Post Minutes to Read:

```jade
    span.post-count= min2read(post.content)
```

Total Count:

```swig
   span.post-count= totalcount(site)
```

## LICENSE

MIT
