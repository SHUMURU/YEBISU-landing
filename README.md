[streamlit_app.py.py](https://github.com/user-attachments/files/26558919/streamlit_app.py.py)# YEBISU-landing[app.py](https://github.com/user-attachments/files/26558650/app.py)
import streamlit as st
import os[save_app.py](https://github.com/user-attachments/files/26559109/save_app.py)import os

# 定义要生成的 Streamlit 代码内容
streamlit_code = """import streamlit as st
import os

# 页面配置
st.set_page_config(
    page_title="YEBISU Premium",
    layout="wide"
)

# 自定义CSS
st.markdown(\"\"\"
<style>
.stApp {
    background: linear-gradient(180deg, #0B0B0B, #1a1a1a);
    color: white;
}
.main-title {
    font-size: 64px;
    font-weight: 600;
    text-align: center;
    color: #D4AF37;
    margin-top: 50px;
}
.sub-title {
    font-size: 24px;
    text-align: center;
    margin-top: 20px;
    color: #cccccc;
}
.center {
    display: flex;
    justify-content: center;
    padding: 20px;
}
.cta-button {
    background-color: #D4AF37;
    color: black !important;
    padding: 12px 40px;
    border-radius: 30px;
    text-decoration: none;
    font-weight: bold;
}
</style>
\"\"\", unsafe_allow_html=True)

st.markdown('<div class="main-title">Premium YEBISU</div>', unsafe_allow_html=True)
st.markdown('<div class="sub-title">本物のビールには、理由がある。</div>', unsafe_allow_html=True)
st.image("https://images.unsplash.com/photo-1532635042-a6f6ad408972?q=80&w=2000", use_container_width=True)

st.markdown('<div class="center"><a href="#" class="cta-button">今すぐ味わう</a></div>', unsafe_allow_html=True)
st.markdown("---")
st.header("Crafted for Perfection")
st.write("厳選された素材、長年の技術、その一杯にすべてが込められている。")

col1, col2 = st.columns(2)
with col1:
    st.image("https://images.unsplash.com/photo-1618889482923-382504ff195e?q=80&w=1000", use_container_width=True)
with col2:
    st.subheader("泡、香り、余韻。")
    st.write("それはただのビールではない。")

st.markdown("---")
st.caption("お酒は20歳になってから。")
"""

# 写入到 streamlit_app.py 文件（Streamlit Cloud 的标准入口文件名）
file_name = "streamlit_app.py"
try:
    with open(file_name, "w", encoding="utf-8") as f:
        f.write(streamlit_code)
    print(f"✅ 成功！文件 '{file_name}' 已创建并保存到当前文件夹。")
    print(f"👉 现在你可以在终端输入 'streamlit run {file_name}' 来查看效果了。")
except Exception as e:
    print(f"❌ 发生错误: {e}")


# 页面配置
st.set_page_config(
    page_title="YEBISU Premium",
    layout="wide"[Uploading simport streamlit as st
import os

# 页面配置
st.set_page_config(
    page_title="YEBISU Premium",
    layout="wide"
)

# 自定义CSS（修正了转义字符，确保样式生效）
st.markdown("""
<style>
.stApp {
    background: linear-gradient(180deg, #0B0B0B, #1a1a1a);
    color: white;
}

.main-title {
    font-size: 64px;
    font-weight: 600;
    text-align: center;
    color: #D4AF37;
    margin-top: 50px;
}

.sub-title {
    font-size: 24px;
    text-align: center;
    margin-top: 20px;
    color: #cccccc;
}

.center {
    display: flex;
    justify-content: center;
    padding: 20px;
}

.cta-button {
    background-color: #D4AF37;
    color: black !important;
    padding: 12px 40px;
    border-radius: 30px;
    text-decoration: none;
    font-weight: bold;
    transition: 0.3s;
}
</style>
""", unsafe_allow_html=True)

# Hero区
st.markdown('<div class="main-title">Premium YEBISU</div>', unsafe_allow_html=True)
st.markdown('<div class="sub-title">本物のビールには、理由がある。</div>', unsafe_allow_html=True)

# 使用高质量的啤酒图片
if os.path.exists("images/hero-beer.jpg"):
    st.image(
        "images/hero-beer.jpg", 
        use_container_width=True,
        caption="至福のひととき"
    )
else:
    st.info("请将 hero-beer.jpg 放在 images 文件夹中")

# 副文案
st.markdown('<div class="sub-title">弟兄の味</div>', unsafe_allow_html=True)

# CTA按钮
st.markdown('<div class="center"><a href="#" class="cta-button">今すぐ味わう</a></div>', unsafe_allow_html=True)

# 分割
st.markdown("---")

# 产品故事
st.header("Crafted for Perfection")

st.write("""
厳選された素材、長年の技術、
その一杯にすべてが込められている。
""")

# 图片展示
col1, col2 = st.columns(2)

with col1:
    if os.path.exists("images/beer-glass.jpg"):
        st.image(
            "images/beer-glass.jpg", 
            use_container_width=True
        )
    else:
        st.info("请将 beer-glass.jpg 放在 images 文件夹中")

with col2:
    st.subheader("泡、香り、余韻。")
    st.write("それはただのビールではない。")

# 底部提示
st.markdown("---")
st.caption("お酒は20歳になってから。")treamlit_app.py.py…]()

)[requirements.txt](https://github.com/user-attachments/files/26558827/requirements.txt)streamlit
openai
anthropic
python-dotenv
watchdog


# 自定义CSS（修正了转义字符，确保样式生效）
st.markdown("""
<style>
.stApp {
    background: linear-gradient(180deg, #0B0B0B, #1a1a1a);
    color: white;
}

.main-title {
    font-size: 64px;
    font-weight: 600;
    text-align: center;
    color: #D4AF37;
    margin-top: 50px;
}

.sub-title {
    font-size: 24px;
    text-align: center;
    margin-top: 20px;
    color: #cccccc;
}

.center {
    display: flex;
    justify-content: center;
    padding: 20px;
}

.cta-button {
    background-color: #D4AF37;
    color: black !important;
    padding: 12px 40px;
    border-radius: 30px;
    text-decoration: none;
    font-weight: bold;
    transition: 0.3s;
}
</style>
""", unsafe_allow_html=True)

# Hero区
st.markdown('<div class="main-title">Premium YEBISU</div>', unsafe_allow_html=True)
st.markdown('<div class="sub-title">本物のビールには、理由がある。</div>', unsafe_allow_html=True)

# 使用高质量的啤酒图片
if os.path.exists("images/hero-beer.jpg"):
    st.image(
        "images/hero-beer.jpg", 
        use_container_width=True,
        caption="至福のひととき"
    )
else:
    st.info("请将 hero-beer.jpg 放在 images 文件夹中")

# 副文案
st.markdown('<div class="sub-title">弟兄の味</div>', unsafe_allow_html=True)

# CTA按钮
st.markdown('<div class="center"><a href="#" class="cta-button">今すぐ味わう</a></div>', unsafe_allow_html=True)

# 分割
st.markdown("---")

# 产品故事
st.header("Crafted for Perfection")

st.write("""
厳選された素材、長年の技術、
その一杯にすべてが込められている。
""")

# 图片展示
col1, col2 = st.columns(2)

with col1:
    if os.path.exists("images/beer-glass.jpg"):
        st.image(
            "images/beer-glass.jpg", 
            use_container_width=True
        )
    else:
        st.info("请将 beer-glass.jpg 放在 images 文件夹中")

with col2:
    st.subheader("泡、香り、余韻。")
    st.write("それはただのビールではない。")

# 底部提示
st.markdown("---")
st.caption("お酒は20歳になってから。")
