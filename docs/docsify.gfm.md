<!-- GFM-TOC -->
* [docsify �̳�](#docsify-�̳�)
    * [ǰ��׼��](#ǰ��׼��)
        * [��װ git](#��װ-git)
        * [��װ npm](#��װ-npm)
        * [��װ notepad++](#��װ-notepad)
    * [��ʼ��](#��ʼ��)
    * [��ҳ�ĵ�](#��ҳ�ĵ�)
    * [�����](#�����)
        * [Ĭ�ϼ��ط�ʽ](#Ĭ�ϼ��ط�ʽ)
        * [�Զ�������ļ���](#�Զ�������ļ���)
    * [Ŀ¼](#Ŀ¼)
    * [������](#������)
        * [HTML ����](#html-����)
        * [Markdown �ļ�����](#markdown-�ļ�����)
        * [Ƕ�ף������б�](#Ƕ�������б�)
    * [����](#����)
        * [Markdown �ļ�����](#markdown-�ļ�����)
    * [����](#����)
        * [�������ҳ](#�������ҳ)
    * [����](#����)
    * [ʾ��](#ʾ��)
<!-- GFM-TOC -->




# docsify �̳�

## ǰ��׼��

### ��װ git

[git ���ھ������ص�ַ](<https://github.com/waylau/git-for-win/>)

### ��װ npm

���� [npm ��װ�̳�](<https://www.cnblogs.com/goldlong/p/8027997.html>)����װ [node](<https://nodejs.org/en/>) ������ѡ�� Long Term Support (LTS) ����֧�ְ汾��

ȫ�ְ�װ `docsify-cli` ���ߣ����Է��㴴��������Ԥ���ĵ���վ��

```
npm i docsify-cli -g
```

### ��װ notepad++

�ı��༭���Ƽ���װ [notepad++](<https://notepad-plus-plus.org/>) ��

## ��ʼ��

�� E:\GitHub �´� git bash here ,ͨ�� `docsify init ./name` ��ʼ����Ŀ���Զ����� E:\GitHub\docsify Ŀ¼�����ڸ�Ŀ¼�»�������������ļ���

- .nojekyll
- index.html
- README.md

```
$ docsify init ./docsify

Initialization succeeded! Please run docsify serve ./docsify
```

`docsify serve docsify`  ���б��ط�������Ĭ�Ϸ��� http://localhost:3000 ʵʱԤ��Ч��

```
$ docsify serve docsify

Serving E:\GitHub\docsify now.
Listening at http://localhost:3000
```

## ��ҳ�ĵ�

```
-| docsify/
  -| README.md
  -| guide.md
  -| zh-cn/
    -| README.md
    -| guide.md
```

��Ӧ�ķ��ʵ�ַΪ

```
docs/README.md        => http://domain.com
docs/guide.md         => http://domain.com/guide
docs/zh-cn/README.md  => http://domain.com/zh-cn/
docs/zh-cn/guide.md   => http://domain.com/zh-cn/guide
```

## �����

### Ĭ�ϼ��ط�ʽ

ͨ�� `_sidebar.md` �ļ�����

�� index.html ������ `loadSidebar` ѡ�Ĭ�ϼ��� `_sidebar.md` �ļ�

```
  <script>
    window.$docsify = {
	  loadSidebar: true
    }
  </script>
```

���Ŵ��� `_sidebar.md` �ļ��������ڸ�Ŀ¼ E:\GitHub\docsify ��

```
* [��ҳ](guide)
* [ָ��](zh-cn/guide)
* [�Զ�����ص��ļ�](summary)
```

 Ч��

![1562813004256](E:\GitHub\CS-Learning\docs\tools\pics\1562813004256.png)

### �Զ�������ļ���

���� `loadSidebar` ѡ��

```
  <script>
    window.$docsify = {
	  loadSidebar: 'summary.md'
    }
  </script>
```

Ч��

![562813148977](E:\GitHub\CS-Learning\docs\tools\pics\1562813148977.png)

## Ŀ¼

���� `subMaxLevel`���������ֱ�ʾ�ܹ���ʾ������ļ���

```
<script>
  window.$docsify = {
    loadSidebar: true,
    subMaxLevel: 2//ֻ����ʾһ����������
  }
</script>
<script src="//unpkg.com/docsify"></script>
```

`{docsify-ignore}` �����ض����⣻`{docsify-ignore-all}` �����ض�ҳ���µ����б��⣻

�޸� E:\GitHub\docsify\guide �ĵ�����

```
1 guide

# һ������0

������ʾ�ڲ����

# һ������1

��ʾ

## ��������1

��ʾ

### ��������1

���õ� subMaxLevel: 2 �����������ⲻ��ʾ

# һ������2

��ʾ

## ��������2{docsify-ignore}

{docsify-ignore} ʡ�Ե�ǰ����

# һ������3{docsify-ignore-all}

{docsify-ignore-all} ʡ���������б���

## ��������3

��ʾ
```

��ʾ������£�

![1562814881526](E:\GitHub\CS-Learning\docs\tools\pics\1562814881526.png)

## ������

���ַ�����HTML ����� Markdown �ļ�����

### HTML ����

ע������Ҫ�� `#/` ��ͷ��

```
<body>
  <nav>//���嵼����
    <a href="#/·��">����������</a>
    <a href="#/">EN</a>
    <a href="#/zh-cn/">����</a>
  </nav>
  <div id="app"></div>
</body>
```

### Markdown �ļ�����

������ `loadNavbar` ��Ĭ�ϼ��ص��ļ�Ϊ `_navbar.md`

```
<script>
  window.$docsify = {
    loadNavbar: true
  }
</script>
<script src="//unpkg.com/docsify"></script>
```

���� `_navbar.md` �������ڸ�Ŀ¼ E:\GitHub\docsify ��

```markdown
* [En](/)
* [����](/zh-cn/)
```

������һ����Ҳ�����Զ�������ļ���

```
window.$docsify = {
  // ���� _navbar.md
  loadNavbar: true,

  // ���� nav.md
  loadNavbar: 'nav.md'
};
```

**Markdown �ļ����õ����ȼ�����ֱ���� HTML �ﶨ��** 

### Ƕ�ף������б�

����������ݹ��࣬����д��Ƕ�׵��б��ᱻ��Ⱦ�������б����ʽ��

�޸�  `_navbar.md` �ļ�

```
- ����1
  - [home 1](/)
  - [guide 1](/guide)

- ����2
  - [home 2](/zh-cn/)
  - [guide 2](/zh-cn/guide)
```

�������ͼ��

![1562817235032](E:\GitHub\CS-Learning\docs\tools\pics\1562817235032.png)

## ����

### Markdown �ļ�����

�޸� `index.html` �ļ�

```
<script>
  window.$docsify = {
    coverpage: true
  }
</script>
<script src="//unpkg.com/docsify"></script>
```

���� `_coverpage.md` �ļ���������ͼƬ������ E:\GitHub\docsify\_medial ·����

```
![logo](_media/logo1)
or
<img width="280px" src="_media/logo1.png">

# docsify

> A magical documentation site generator.

* Simple and lightweight (~12kb gzipped)
* Multiple themes
* Not build static html files

[GitHub](https://github.com/docsifyjs/docsify/)
[Get Started](#quick-start)
```

һ���ĵ�ֻ���ڸ�Ŀ¼�¼��ط��棬����ҳ����߶���Ŀ¼�¶�������ء�

## ����

Ĭ�ϵı�����������ɵĽ���ɫ�������Զ��屳��ɫ���߱���ͼ�����ĵ�ĩβ�����ͼƬ�� Markdown �﷨���ñ�����

`_coverpage.md`

```
<!-- ����ͼƬ -->

![](_media/bg.png)

<!-- ����ɫ -->

![color](#f0f0f0)
```

### �������ҳ

```
window.$docsify = {
  coverpage: true,

  // �Զ����ļ���
  coverpage: 'cover.md',

  // mutiple covers
  coverpage: ['/', '/zh-cn/'],

  // mutiple covers and custom file name
  coverpage: {
    '/': 'cover.md',
    '/zh-cn/': 'cover.md'
  }
};
```

## ����

������ϸ˵�����գ�

[�ٷ�˵���ĵ�-Ӣ�İ�](<https://docsify.js.org/#/>)

[�ٷ�˵���ĵ�-���İ�](<https://docsify.js.org/#/zh-cn/>)

## ʾ��

[������Ŀ���� GitHub �� fork](<https://github.com/dreamwhigh/CS-Learning>)

���� index.html ���������£�

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>CS-Learning</title>
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
  <meta name="description" content="Description">
  <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
  <link rel="stylesheet" href="//unpkg.com/docsify/lib/themes/vue.css">
</head>
<body>
  <div id="app"></div>
  <script>
    window.$docsify = {
		maxAge: 100,
		name: 'CS-Learning',//�ĵ���
		repo: 'dreamwhigh/CS-Learning',//Github corner �Ҽ�
		loadSidebar: true,//���ò����
		subMaxLevel: 2,//����Ŀ¼�����⼶��
		maxLevel: 3,
		loadNavbar: true,//���õ�����
		coverpage: true,//���÷���
        search: {
            paths: 'auto',
            placeholder: '? Type to search ',
            noData: '? No Results! ',
            // Headline depth, 1 - 6
            depth: 6
        },//����������
    }
  </script>
  <script src="//unpkg.com/docsify/lib/docsify.min.js"></script>
  <script src="//unpkg.com/docsify/lib/plugins/search.min.js"></script>
  <script src="//unpkg.com/prismjs/components/prism-java.min.js"></script>
  <script src="//unpkg.com/docsify/lib/plugins/zoom-image.js"></script>
  <script src="//unpkg.com/docsify-copy-code"></script>
  <script src="//unpkg.com/docsify-pagination/dist/docsify-pagination.min.js"></script>
</body>
</html>

```
