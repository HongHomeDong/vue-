 # vue-quill-editor 
 
 ## 1 npm 安装 vue-quill-editor 
 
 ## 2 在模板中引入
 
 ###  
         <template>
               <quill-editor 
                v-model="content" 
                ref="myQuillEditor" 
                :options="editorOption" 
                @blur="onEditorBlur($event)" @focus="onEditorFocus($event)"
                @change="onEditorChange($event)">
              </quill-editor>
          </template> 
          import { quillEditor } from 'vue-quill-editor'
 ## 3 option的配置
 
 ###1.只需要填写功能名的
    加粗 - bold；
    斜体 - italic
    下划线 - underline
    删除线 - strike
    引用- blockquote
    代码块 - code-block
    公式 - formula
    图片 - image
    视频 - video
    清除字体样式- clean
    这一类的引用 直接['name','name']这种格式就好了
    
    2.需要有默认值的
    标题 - header  
    [{ 'header': 1 }, { 'header': 2 }] 值字体大小
    
    列表 - list 
    [{ 'list': 'ordered'}, { 'list': 'bullet' }], 值ordered，bullet
    
    上标/下标 - script 
     [{ 'script': 'sub'}, { 'script': 'super' }],  值sub，super
    
    缩进 - indent
    [{ 'indent': '-1'}, { 'indent': '+1' }], 值-1，+1等
    
    文本方向 - direction
    [{ 'direction': 'rtl' }],    值rtl
    有多个值 以下拉列表形式显示
   
    大小 - size
    [{ 'size': ['small', false, 'large', 'huge'] }],  
    
    标题 - header
    [{ 'header': [1, 2, 3, 4, 5, 6, false] }],
    
    有系统默认值的功能只需填写一个空数组 就会有出现默认的选项
    颜色 - color
    背景颜色 - background
    字体 - font
    文本对齐 - align
    他们的格式都是
    [{ 'color': [] }, { 'background': [] }], 
    [{ 'font': [] }],
    [{ 'align': [] }]
    这种格式