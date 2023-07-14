<div class="blog-content-box">
    <div class="article-header-box">
        <div class="article-header">
            <div class="article-title-box">
                <h1 class="title-article" id="articleContentId">c语言attribute关键字参数（详细）总结附示例快速掌握</h1>
            </div>
            <div class="article-info-box">
                <div class="article-bar-top">
                    <img class="article-type-img" src="https://csdnimg.cn/release/blogv2/dist/pc/img/original.png" alt="">
                    <div class="bar-content">
                      <a class="follow-nickName " href="https://blog.csdn.net/Luckiers" target="_blank" rel="noopener" title="快乐的学习">快乐的学习</a>
                    <img class="article-time-img article-heard-img" src="https://csdnimg.cn/release/blogv2/dist/pc/img/newCurrentTime2.png" alt="">
                        <span class="time">于&nbsp;2023-01-19 23:31:03&nbsp;发布</span>
                    <img class="article-read-img article-heard-img" src="https://csdnimg.cn/release/blogv2/dist/pc/img/articleReadEyes2.png" alt="">
                    <span class="read-count">2195</span>
                    <a id="blog_detail_zk_collection" class="un-collection" data-report-click="{&quot;mod&quot;:&quot;popu_823&quot;,&quot;spm&quot;:&quot;1001.2101.3001.4232&quot;,&quot;ab&quot;:&quot;new&quot;}">
                        <img class="article-collect-img article-heard-img un-collect-status isdefault" style="display:inline-block" src="https://csdnimg.cn/release/blogv2/dist/pc/img/tobarCollect2.png" alt="">
                        <img class="article-collect-img article-heard-img collect-status isactive" style="display:none" src="https://csdnimg.cn/release/blogv2/dist/pc/img/tobarCollectionActive2.png" alt="">
                        <span class="name">收藏</span>
                        <span class="get-collection" style="color: rgb(153, 154, 170);">
                            15
                        </span>
                    </a>
                    </div>
                </div>
                <div class="blog-tags-box">
                    <div class="tags-box artic-tag-box">
                            <span class="label">分类专栏：</span>
                                <a class="tag-link" href="https://blog.csdn.net/luckiers/category_11864986.html" target="_blank" rel="noopener">c语言</a>
                            <span class="label">文章标签：</span>
                                <a data-report-click="{&quot;mod&quot;:&quot;popu_626&quot;,&quot;spm&quot;:&quot;1001.2101.3001.4223&quot;,&quot;strategy&quot;:&quot;c语言&quot;,&quot;ab&quot;:&quot;new&quot;,&quot;extra&quot;:&quot;{\&quot;searchword\&quot;:\&quot;c语言\&quot;}&quot;}" class="tag-link" href="https://so.csdn.net/so/search/s.do?q=c%E8%AF%AD%E8%A8%80&amp;t=all&amp;o=vip&amp;s=&amp;l=&amp;f=&amp;viparticle=" target="_blank" rel="noopener">c语言</a>
                                <a data-report-click="{&quot;mod&quot;:&quot;popu_626&quot;,&quot;spm&quot;:&quot;1001.2101.3001.4223&quot;,&quot;strategy&quot;:&quot;开发语言&quot;,&quot;ab&quot;:&quot;new&quot;,&quot;extra&quot;:&quot;{\&quot;searchword\&quot;:\&quot;开发语言\&quot;}&quot;}" class="tag-link" href="https://so.csdn.net/so/search/s.do?q=%E5%BC%80%E5%8F%91%E8%AF%AD%E8%A8%80&amp;t=all&amp;o=vip&amp;s=&amp;l=&amp;f=&amp;viparticle=" target="_blank" rel="noopener">开发语言</a>
                    </div>
                </div>
                <div class="slide-content-box">
                    <div class="article-copyright">
                        <div class="creativecommons">
                            版权声明：本文为博主原创文章，遵循<a href="http://creativecommons.org/licenses/by-sa/4.0/" target="_blank" rel="noopener"> CC 4.0 BY-SA </a>版权协议，转载请附上原文出处链接和本声明。
                        </div>
                        <div class="article-source-link">
                            本文链接：<a href="https://blog.csdn.net/Luckiers/article/details/128737046" target="_blank">https://blog.csdn.net/Luckiers/article/details/128737046</a>
                        </div>
                    </div>
                </div>
<div class="toc"> 
 <h3><a name="t0"></a>目录</h3> 
 <ul><li><ul><li><a href="#_1" target="_self">一、简介</a></li><li><a href="#_12" target="_self">二、参数详解</a></li><li><ul><li><a href="#21_section_13" target="_self">2.1 section：自定义段</a></li><li><a href="#22_aligned_30" target="_self">2.2 aligned：对齐</a></li><li><a href="#23_packed_37" target="_self">2.3 packed：对齐</a></li><li><a href="#24_format_41" target="_self">2.4 format：检查函数变参格式</a></li><li><a href="#25_used_55" target="_self">2.5 used</a></li><li><a href="#26_unused_74" target="_self">2.6 unused</a></li><li><a href="#27_at__81" target="_self">2.7 at 绝对定位</a></li><li><a href="#28_constructor_91" target="_self">2.8 constructor</a></li><li><a href="#29_destructor_130" target="_self">2.9 destructor</a></li><li><a href="#210_weak_132" target="_self">2.10 weak：弱声明</a></li><li><a href="#211_alias_181" target="_self">2.11 alias：函数起别名</a></li><li><a href="#212_always_inline_197" target="_self">2.12 always_inline：内联函数总是展开</a></li><li><a href="#213_noinline_212" target="_self">2.13 noinline：无内联</a></li><li><a href="#214_transparent_union_215" target="_self">2.14 transparent_union</a></li><li><a href="#215_deprecated_217" target="_self">2.15 deprecated</a></li><li><a href="#216_noreturn_227" target="_self">2.16 noreturn</a></li></ul> 
   </li><li><a href="#_231" target="_self">三、其他相关链接</a></li></ul> 
 </li></ul> 
</div> 
<p></p> 
<h2><a name="t1"></a><a id="_1"></a>一、简介</h2> 
<p><a href="https://so.csdn.net/so/search?q=GNU&amp;spm=1001.2101.3001.7020" target="_blank" class="hl hl-1" data-report-click="{&quot;spm&quot;:&quot;1001.2101.3001.7020&quot;,&quot;dest&quot;:&quot;https://so.csdn.net/so/search?q=GNU&amp;spm=1001.2101.3001.7020&quot;,&quot;extra&quot;:&quot;{\&quot;searchword\&quot;:\&quot;GNU\&quot;}&quot;}" data-tit="GNU" data-pretit="gnu">GNU</a> C编译器增加了一个__attribute__ 关键字用来声明一个函数、变量或类型的特殊属性。申明这些属性主要用途就是指导编译程序进行特定方面的优化或代码检查。<br> attribute 可以设置函数属性（Function Attribute ）、变量属性（Variable Attribute ）和类型属性（Type Attribute ）。<br> 关键字<a href="https://so.csdn.net/so/search?q=__attribute__&amp;spm=1001.2101.3001.7020" target="_blank" class="hl hl-1" data-report-click="{&quot;spm&quot;:&quot;1001.2101.3001.7020&quot;,&quot;dest&quot;:&quot;https://so.csdn.net/so/search?q=__attribute__&amp;spm=1001.2101.3001.7020&quot;,&quot;extra&quot;:&quot;{\&quot;searchword\&quot;:\&quot;__attribute__\&quot;}&quot;}" data-tit="__attribute__" data-pretit="__attribute__">__attribute__</a> 也可以对结构体（struct ）或共用体（union ）进行属性设置。<br> attribute 书写特征是：attribute 前后都有两个下划线，并切后面会紧跟一对原括弧，括弧里面是相应的__attribute__ 参数，格式如下：</p> 
<pre data-index="0" class="prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"> <span class="token keyword">__attribute__</span> <span class="token punctuation">(</span><span class="token punctuation">(</span>ATTRIBUTE<span class="token punctuation">)</span><span class="token punctuation">)</span>
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li></ul></pre> 
<h2><a name="t2"></a><a id="_12"></a>二、参数详解</h2> 
<h3><a name="t3"></a><a id="21_section_13"></a>2.1 section：自定义段</h3> 
<p>section属性的主要作用是：在程序编译时，将一个函数或者变量放到指定的段，即指定的section中。<br> 一个可执行文件注意由代码段，数据段、bss段构成。代码段主要用来存放编译生成的可执行指令代码、数据段和bss段用来存放全局变量和未初始化的全局变量。<br> 除了这三个段，可执行文件还包含一些其他的段。我们可以用 readelf 去查看一个可执行文件各个section信息。</p> 
<pre data-index="1" class="prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"><span class="token keyword">int</span> global_val <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
<span class="token keyword">int</span> unint_val <span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token function">section</span><span class="token punctuation">(</span><span class="token string">".data"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">int</span> <span class="token function">main</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
<span class="token punctuation">{<!-- --></span>
    <span class="token keyword">return</span> <span class="token number">0</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li></ul></pre> 
<p><img src="https://img-blog.csdnimg.cn/8fd9e6449f1d4659870864ed25939be2.png" alt="在这里插入图片描述"></p> 
<h3><a name="t4"></a><a id="22_aligned_30"></a>2.2 aligned：对齐</h3> 
<p>GNU C 通过 __attribute__ 来声明 aligned 和 packed 属性，指定一个变量或类型的对齐方式。</p> 
<p>通过aligned属性，我们可以显示地指定变量在内存中的地址对齐方式。aligned有一个参数，表示要按几个字节对齐，使用时要注意，地址对齐的字节数必须是 2 的幂次方，否则编译就会报错。</p> 
<p><img src="https://img-blog.csdnimg.cn/2dbbd61488174180922c59b3bca367f3.png" alt="在这里插入图片描述"></p> 
<h3><a name="t5"></a><a id="23_packed_37"></a>2.3 packed：对齐</h3> 
<p><img src="https://img-blog.csdnimg.cn/b34e9ecdfff840bbb59bd9fdab364c9a.png" alt="在这里插入图片描述"><strong>aligned 属性一般用来增大变量的地址对齐，元素之间地址对齐会造成一定的内存空洞，而packed属性则正好相反，一般用来减少地址对齐，指定变量或类型使用最可能小的地址对齐方式。</strong></p> 
<h3><a name="t6"></a><a id="24_format_41"></a>2.4 format：检查函数变参格式</h3> 
<p>指定变参函数的参数格式检查</p> 
<pre data-index="2" class="prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"><span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token function">format</span> <span class="token punctuation">(</span>archetype<span class="token punctuation">,</span> string<span class="token operator">-</span>index<span class="token punctuation">,</span> frist<span class="token operator">-</span>to<span class="token operator">-</span>check<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
<span class="token keyword">void</span> <span class="token function">LOG</span><span class="token punctuation">(</span><span class="token keyword">const</span> <span class="token keyword">char</span> <span class="token operator">*</span>fmt<span class="token punctuation">,</span> <span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">)</span> <span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token function">format</span><span class="token punctuation">(</span>printf<span class="token punctuation">,</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li></ul></pre> 
<p>属性format(printf,1,2) 有3个参数，第一个参数pritnf 是告诉编译器，按照printf的标准来检查；第二个参数表示LOG()函数所有的参数列表中格式字符串的位置索引，第三个参数是告诉编译器要检查的参数的起始位置。</p> 
<pre data-index="3" class="prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"><span class="token function">LOG</span><span class="token punctuation">(</span><span class="token string">"hello world ,i am %d ages "</span><span class="token punctuation">,</span> age<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">/* 前者表示格式字符串，后者表示所有的参数*/</span>
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li></ul></pre> 
<h3><a name="t7"></a><a id="25_used_55"></a>2.5 used</h3> 
<p>used的作用是告诉编译器，我声明的这个符号是需要保留的。被used修饰以后，意味着即使函数没有被引用，在Release下也不会被优化。如果不加这个修饰，那么Release环境链接器会去掉没有被引用的段。<br> 1、这个函数属性通知编译器在目标文件中保留一个静态函数，即使它没有被引用；<br> 2、标记为attribute__((used))的函数被标记在目标文件中，以避免链接器删除未使用的节；<br> 3、静态变量也可以标记为used，方法是使用 attribute((used))。</p> 
<pre data-index="4" class="prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"><span class="token keyword">static</span> <span class="token keyword">int</span> <span class="token function">lose_this</span><span class="token punctuation">(</span><span class="token keyword">int</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">static</span> <span class="token keyword">int</span> <span class="token function">keep_this</span><span class="token punctuation">(</span><span class="token keyword">int</span><span class="token punctuation">)</span> <span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span>used<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>     <span class="token comment">// retained in object file</span>

<span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span>used<span class="token punctuation">,</span><span class="token function">section</span><span class="token punctuation">(</span><span class="token string">".rodata.$AppID"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
<span class="token keyword">const</span> <span class="token class-name">uint8_t</span>   ApplicationID<span class="token punctuation">[</span><span class="token number">16</span><span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token punctuation">{<!-- --></span>
        <span class="token number">0x00</span><span class="token punctuation">,</span> <span class="token number">0x00</span><span class="token punctuation">,</span> <span class="token number">0x00</span><span class="token punctuation">,</span> <span class="token number">0x00</span><span class="token punctuation">,</span>
        <span class="token number">0x00</span><span class="token punctuation">,</span> <span class="token number">0x00</span><span class="token punctuation">,</span> <span class="token number">0x00</span><span class="token punctuation">,</span> <span class="token number">0x00</span><span class="token punctuation">,</span>
        <span class="token number">0x00</span><span class="token punctuation">,</span> <span class="token number">0x00</span><span class="token punctuation">,</span> <span class="token number">0x00</span><span class="token punctuation">,</span> <span class="token number">0x00</span><span class="token punctuation">,</span>
        <span class="token number">0x12</span><span class="token punctuation">,</span> <span class="token number">0x34</span><span class="token punctuation">,</span> <span class="token number">0x00</span><span class="token punctuation">,</span> <span class="token number">0x00</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span>
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li><li style="color: rgb(153, 153, 153);">8</li><li style="color: rgb(153, 153, 153);">9</li><li style="color: rgb(153, 153, 153);">10</li></ul></pre> 
<h3><a name="t8"></a><a id="26_unused_74"></a>2.6 unused</h3> 
<p>表示该函数或变量可能不使用，这个属性可以避免编译器产生警告信息。</p> 
<pre data-index="5" class="prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"><span class="token macro property"><span class="token directive-hash">#</span><span class="token directive keyword">define</span> <span class="token macro-name">__attribute_unused__</span> <span class="token expression"><span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span>__unused__<span class="token punctuation">)</span><span class="token punctuation">)</span></span></span>
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li></ul></pre> 
<h3><a name="t9"></a><a id="27_at__81"></a>2.7 at 绝对定位</h3> 
<p>绝对定位，可以把变量或函数绝对定位到Flash中，或者定位到RAM。<br> 定位到flash中，一般用于固化的信息，如出厂设置的参数，上位机配置的参数，ID卡的ID号，flash标记等等。</p> 
<pre data-index="6" class="prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"><span class="token keyword">const</span> u16 gFlashDefValue<span class="token punctuation">[</span><span class="token number">512</span><span class="token punctuation">]</span> <span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token function">at</span><span class="token punctuation">(</span><span class="token number">0x0800F000</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">=</span> <span class="token punctuation">{<!-- --></span><span class="token number">0x1111</span><span class="token punctuation">,</span><span class="token number">0x1111</span><span class="token punctuation">,</span><span class="token number">0x1111</span><span class="token punctuation">,</span><span class="token number">0x0111</span><span class="token punctuation">,</span><span class="token number">0x0111</span><span class="token punctuation">,</span><span class="token number">0x0111</span><span class="token punctuation">}</span><span class="token punctuation">;</span><span class="token comment">//定位在flash中,其他flash补充为00</span>
<span class="token keyword">const</span> u16 <span class="token function">gflashdata__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token function">at</span><span class="token punctuation">(</span><span class="token number">0x0800F000</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">=</span> <span class="token number">0xFFFF</span><span class="token punctuation">;</span>

<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li></ul></pre> 
<h3><a name="t10"></a><a id="28_constructor_91"></a>2.8 constructor</h3> 
<p>确保此函数在main函数被调用之前调用<br> constructor和destructor会在ELF文件中添加两个段-.ctors和.dtors。当动态库或程序在加载时，会检查是否存在这两个段，如果存在执行对应的代码。</p> 
<pre data-index="7" class="prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"><span class="token keyword">int</span> <span class="token function">main</span><span class="token punctuation">(</span><span class="token keyword">int</span> argc<span class="token punctuation">,</span> <span class="token keyword">char</span> <span class="token operator">*</span> argv<span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">)</span> <span class="token punctuation">{<!-- --></span>
    @autoreleasepool <span class="token punctuation">{<!-- --></span>
        <span class="token function">printf</span><span class="token punctuation">(</span><span class="token string">"main function"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token keyword">return</span> <span class="token function">UIApplicationMain</span><span class="token punctuation">(</span>argc<span class="token punctuation">,</span> argv<span class="token punctuation">,</span> nil<span class="token punctuation">,</span> <span class="token function">NSStringFromClass</span><span class="token punctuation">(</span><span class="token punctuation">[</span>AppDelegate class<span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
<span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span>constructor<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token keyword">static</span> <span class="token keyword">void</span> <span class="token function">beforeFunction</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
<span class="token punctuation">{<!-- --></span>
    <span class="token function">printf</span><span class="token punctuation">(</span><span class="token string">"beforeFunction\n"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li><li style="color: rgb(153, 153, 153);">8</li><li style="color: rgb(153, 153, 153);">9</li><li style="color: rgb(153, 153, 153);">10</li></ul></pre> 
<p>打印结果如下：</p> 
<pre data-index="8" class="prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;">beforeFunction
main function
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li></ul></pre> 
<pre data-index="9" class="prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"><span class="token keyword">static</span>  <span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token function">constructor</span><span class="token punctuation">(</span><span class="token number">101</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token keyword">void</span> <span class="token function">before1</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
<span class="token punctuation">{<!-- --></span>
        <span class="token function">printf</span><span class="token punctuation">(</span><span class="token string">"before1\n"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<span class="token keyword">static</span>  <span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token function">constructor</span><span class="token punctuation">(</span><span class="token number">102</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token keyword">void</span> <span class="token function">before2</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
<span class="token punctuation">{<!-- --></span>
        <span class="token function">printf</span><span class="token punctuation">(</span><span class="token string">"before2\n"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<span class="token keyword">static</span>  <span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token function">constructor</span><span class="token punctuation">(</span><span class="token number">102</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token keyword">void</span> <span class="token function">before3</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
<span class="token punctuation">{<!-- --></span>
        <span class="token function">printf</span><span class="token punctuation">(</span><span class="token string">"before3\n"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li><li style="color: rgb(153, 153, 153);">8</li><li style="color: rgb(153, 153, 153);">9</li><li style="color: rgb(153, 153, 153);">10</li><li style="color: rgb(153, 153, 153);">11</li><li style="color: rgb(153, 153, 153);">12</li></ul></pre> 
<p>以上三个函数会依照优先级的顺序调用.另外,我以前看过,这个1-100的范围是保留的,所以,最好从100之后开始用。</p> 
<h3><a name="t11"></a><a id="29_destructor_130"></a>2.9 destructor</h3> 
<p>确保此函数在main()函数退出或者调用了exit()之后,调用我们的函数。</p> 
<h3><a name="t12"></a><a id="210_weak_132"></a>2.10 weak：弱声明</h3> 
<p>将一个强符号，转换为弱符号。使用方法如下：</p> 
<pre data-index="10" class="prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"><span class="token keyword">void</span> <span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span>weak<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token function">func</span><span class="token punctuation">(</span><span class="token keyword">void</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">int</span> num <span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span>weak<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li></ul></pre> 
<p>在一个程序中，无论是变量名，还是函数名，在编译器眼里，就是一个符号而已，符号可以分为强符号和弱符号。<br> 强符号：函数名，初始化的全局变量名<br> 弱符号：未初始化的全局变量名。</p> 
<pre data-index="11" class="set-code-hide prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"><span class="token comment">//func1.c</span>
<span class="token keyword">int</span> a <span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span>weak<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span>
<span class="token keyword">void</span> <span class="token function">func</span><span class="token punctuation">(</span><span class="token keyword">void</span><span class="token punctuation">)</span>
<span class="token punctuation">{<!-- --></span>
    <span class="token function">printf</span><span class="token punctuation">(</span><span class="token string">"func.a = %d\n"</span><span class="token punctuation">,</span> a<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token comment">//main.c</span>
<span class="token keyword">int</span> a <span class="token operator">=</span> <span class="token number">4</span><span class="token punctuation">;</span>
<span class="token keyword">void</span> <span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span>weak<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token function">func</span><span class="token punctuation">(</span><span class="token keyword">void</span><span class="token punctuation">)</span>
<span class="token punctuation">{<!-- --></span>
    <span class="token function">printf</span><span class="token punctuation">(</span><span class="token string">"main.a = %d\n"</span><span class="token punctuation">,</span> a<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token keyword">int</span> <span class="token function">main</span><span class="token punctuation">(</span><span class="token keyword">void</span><span class="token punctuation">)</span>
<span class="token punctuation">{<!-- --></span>
   <span class="token function">func</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
   <span class="token keyword">return</span> <span class="token number">0</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<div class="hljs-button {2}" data-title="复制"></div></code><div class="hide-preCode-box"><span class="hide-preCode-bt"><img class="look-more-preCode contentImg-no-view" src="https://csdnimg.cn/release/blogv2/dist/pc/img/newCodeMoreWhite.png" alt="" title=""></span></div><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li><li style="color: rgb(153, 153, 153);">8</li><li style="color: rgb(153, 153, 153);">9</li><li style="color: rgb(153, 153, 153);">10</li><li style="color: rgb(153, 153, 153);">11</li><li style="color: rgb(153, 153, 153);">12</li><li style="color: rgb(153, 153, 153);">13</li><li style="color: rgb(153, 153, 153);">14</li><li style="color: rgb(153, 153, 153);">15</li><li style="color: rgb(153, 153, 153);">16</li><li style="color: rgb(153, 153, 153);">17</li><li style="color: rgb(153, 153, 153);">18</li><li style="color: rgb(153, 153, 153);">19</li></ul></pre> 
<p><strong>弱符号的用途</strong><br> 1、在一个源文件中引用一个编号或者函数，当编译器只看到声明，而没看到其定义时，一般编译时不会报错。在链接阶段，链接器会到其他文件中找到这些符号的定义，若未找到，则报未定义错误。</p> 
<p>2、当函数被声明一个弱符号时，会有一个奇特地方：当链接器找不到这个函数的定义时，也不会报错。编译器会将这个函数名，即弱符号，设置为0或者一个特殊值。只有当程序运行时，调用到这个函数，跳转到零地址或者一个特殊的地址才会报错误，产生一个内存错误。</p> 
<p>3、如果我们在使用函数前，判断这个函数地址是否为0，即可避免段错误。你会发现，即使函数未定义也可以正常编过。</p> 
<p>4、弱符号的这个特性在库函数开发设计中应用十分广泛，如果在开发一个库时，基础功能已经实现，有些高级功能还未实现，那么你就可以将这些函数通过weak 属性声明转换为一个弱符号。</p> 
<p>符号(或弱定义) weak属性只会在静态库(.o .a )中生效，动态库(.so)中不会生效</p> 
<pre data-index="12" class="prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"><span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token function">weakref</span><span class="token punctuation">(</span>“别名”<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li></ul></pre> 
<p>//引用,必须是static类型，别名要写，不然等效于weak（其实也可以直接写成weak的形式）</p> 
<h3><a name="t13"></a><a id="211_alias_181"></a>2.11 alias：函数起别名</h3> 
<p>主要用来给函数定义一个别名</p> 
<pre data-index="13" class="prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"><span class="token keyword">void</span> <span class="token function">__f</span><span class="token punctuation">(</span><span class="token keyword">void</span><span class="token punctuation">)</span>
<span class="token punctuation">{<!-- --></span>
    <span class="token function">printf</span><span class="token punctuation">(</span><span class="token string">"__f\n"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token keyword">void</span> <span class="token function">f</span><span class="token punctuation">(</span><span class="token keyword">void</span><span class="token punctuation">)</span> <span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span><span class="token function">alias</span><span class="token punctuation">(</span><span class="token string">"__f"</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">int</span> <span class="token function">main</span><span class="token punctuation">(</span><span class="token keyword">void</span><span class="token punctuation">)</span>
<span class="token punctuation">{<!-- --></span>
    <span class="token function">f</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">return</span> <span class="token number">0</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li><li style="color: rgb(153, 153, 153);">6</li><li style="color: rgb(153, 153, 153);">7</li><li style="color: rgb(153, 153, 153);">8</li><li style="color: rgb(153, 153, 153);">9</li><li style="color: rgb(153, 153, 153);">10</li><li style="color: rgb(153, 153, 153);">11</li></ul></pre> 
<h3><a name="t14"></a><a id="212_always_inline_197"></a>2.12 always_inline：内联函数总是展开</h3> 
<p>说起内联函数，就不得不说起函数调用开销。一个函数在执行过程中，如果要调用其他函数，则一般会执行以下过程：<br> 1、保存当前函数现场；<br> 2、跳到调用函数执行；<br> 3、恢复当前函数现场；<br> 4、继续执行当前函数；<br> 对于一些短小精悍，并且调用频繁的函数，调用开销大，这个时候我们可以将函数声明为内联函数。编译器遇到内联函数会想宏一样将内联函数之间在调用处展开，这样做就减少了函数调用的开销。<br> 当我们认为一个函数体积小、而且被大量调用，应做内联展开时，就可以使用static inline 关键字修饰它，但是编译器不一定会内联展开。如果想明确告诉编译器一定要展开，或者不展开就可以使用 noinline 和 always_inline 对函数的属性做一个声明。<br> 内联的本质是用代码块直接替换掉函数调用处，好处是:快代码的执行，减少系统开销。</p> 
<pre data-index="14" class="prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"><span class="token keyword">void</span> <span class="token function">test</span><span class="token punctuation">(</span><span class="token keyword">int</span> a<span class="token punctuation">)</span><span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span>always_inline<span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li></ul></pre> 
<h3><a name="t15"></a><a id="213_noinline_212"></a>2.13 noinline：无内联</h3> 
<p>与always_inline相反，无内联展开</p> 
<h3><a name="t16"></a><a id="214_transparent_union_215"></a>2.14 transparent_union</h3> 
<p>我们可以使用透明联合类型，函数指针能够指向参数类型不同的函数。</p> 
<h3><a name="t17"></a><a id="215_deprecated_217"></a>2.15 deprecated</h3> 
<p>如果被变量或者函数的声明使用deprecated属性进行描述，那么编译器编译过程中不会产生警告或者错误，但是，被该属性描述的变量或者函数在其他地方被调用，那么编译会产生警告，警告信息中包含过时接口定义的位置及代码中的引用位置。</p> 
<pre data-index="15" class="prettyprint"><code class="prism language-c has-numbering" onclick="mdcp.copyCode(event)" style="position: unset;"><span class="token macro property"><span class="token directive-hash">#</span><span class="token directive keyword">define</span> <span class="token macro-name">attribute_deprecated</span> <span class="token expression"><span class="token keyword">__attribute__</span><span class="token punctuation">(</span><span class="token punctuation">(</span>deprecated<span class="token punctuation">)</span><span class="token punctuation">)</span></span></span>
<span class="token comment">/* Variable Attribute */</span>
attribute_deprecated <span class="token keyword">int</span>  variable_old <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span>
<span class="token comment">/* Function Attribute */</span>
attribute_deprecated <span class="token keyword">void</span> <span class="token function">function_old</span><span class="token punctuation">(</span><span class="token keyword">void</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<div class="hljs-button {2}" data-title="复制"></div></code><ul class="pre-numbering" style=""><li style="color: rgb(153, 153, 153);">1</li><li style="color: rgb(153, 153, 153);">2</li><li style="color: rgb(153, 153, 153);">3</li><li style="color: rgb(153, 153, 153);">4</li><li style="color: rgb(153, 153, 153);">5</li></ul></pre> 
<h3><a name="t18"></a><a id="216_noreturn_227"></a>2.16 noreturn</h3> 
<p>几个标注库函数，例如abort exit，没有返回值。GCC能够自动识别这种情况。noreturn属性指定像这样的任何不需要返回值的函数。当遇到类似函数还未运行到return语句就需要退出来的情况，该属性可以避免出现错误信息。</p> 
<h2><a name="t19"></a><a id="_231"></a>三、其他相关链接</h2> 
<p><a href="https://blog.csdn.net/Luckiers/article/details/125277326"><strong>1、C语言常用函数详细总结</strong></a></p> 
<p><a href="https://blog.csdn.net/Luckiers/article/details/125265226"><strong>2、C语言中指针、数组作为作为函数参数使用总结</strong></a></p> 
<p><a href="https://blog.csdn.net/Luckiers/article/details/125253835"><strong>3、C语言常见数据类型字节数和打印格式总结</strong></a></p> 
<p><a href="https://blog.csdn.net/Luckiers/article/details/126436049"><strong>4、C语言、Makefile和shell中添加打印调试信息总结</strong></a></p> 
<p><a href="https://blog.csdn.net/Luckiers/article/details/127401628"><strong>5、c语言volatile关键字总结</strong></a></p>
                </div><div><div></div></div>
                <link href="https://csdnimg.cn/release/blogv2/dist/mdeditor/css/editerView/markdown_views-98b95bb57c.css" rel="stylesheet">
                <link href="https://csdnimg.cn/release/blogv2/dist/mdeditor/css/style-c216769e99.css" rel="stylesheet">
        </div>
        <div id="treeSkill" style="display: block;"><div class="skill-tree-box"><div class="skill-tree-head">文章知识点与官方知识档案匹配，可进一步学习相关知识</div><div class="skill-tree-body"><div class="skill-tree-item"><span class="skill-tree-href"><a data-report-click="{&quot;spm&quot;:&quot;1001.2101.3001.6866&quot;,&quot;dest&quot;:&quot;https://edu.csdn.net/skill/c/?utm_source=csdn_ai_skill_tree_blog&quot;}" href="https://edu.csdn.net/skill/c/?utm_source=csdn_ai_skill_tree_blog" target="_blank">C技能树</a><i></i><a data-report-click="{&quot;spm&quot;:&quot;1001.2101.3001.6866&quot;,&quot;dest&quot;:&quot;https://edu.csdn.net/skill/c/?utm_source=csdn_ai_skill_tree_blog&quot;}" href="https://edu.csdn.net/skill/c/?utm_source=csdn_ai_skill_tree_blog" target="_blank">首页</a><i></i><a data-report-click="{&quot;spm&quot;:&quot;1001.2101.3001.6866&quot;,&quot;dest&quot;:&quot;https://edu.csdn.net/skill/c/?utm_source=csdn_ai_skill_tree_blog&quot;}" href="https://edu.csdn.net/skill/c/?utm_source=csdn_ai_skill_tree_blog" target="_blank">概览</a></span><span class="skill-tree-con"><span class="skill-tree-count">155440</span> 人正在系统学习中</span></div></div></div></div>
    </article>
<script>
  $(function() {
    setTimeout(function () {
      var mathcodeList = document.querySelectorAll('.htmledit_views img.mathcode');
      if (mathcodeList.length > 0) {
        for (let i = 0; i < mathcodeList.length; i++) {
          if (mathcodeList[i].naturalWidth === 0 || mathcodeList[i].naturalHeight === 0) {
            var alt = mathcodeList[i].alt;
            alt = '\\(' + alt + '\\)';
            var curSpan = $('<span class="img-codecogs"></span>');
            curSpan.text(alt);
            $(mathcodeList[i]).before(curSpan);
            $(mathcodeList[i]).remove();
          }
        }
        MathJax.Hub.Queue(["Typeset",MathJax.Hub]);
      }
    }, 1000)
  });
</script>
</div>