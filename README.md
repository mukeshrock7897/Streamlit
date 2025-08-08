
---

# 🌀 **Streamlit v1.47.0**

---

## ✅ 1. **Introduction to Streamlit**

| Concept            | Description                                               |
| ------------------ | --------------------------------------------------------- |
| What is Streamlit? | Lightweight framework for building ML/Data apps           |
| Core Use           | Rapid prototyping of ML dashboards, UI for Python scripts |
| Key Feature        | Pure Python syntax, auto-refresh UI, minimal setup        |

---

## 🖼️ 2. **Basic App Structure**

| Topic                       | Description                       |
| --------------------------- | --------------------------------- |
| `streamlit run app.py`      | Launch app                        |
| `if __name__ == "__main__"` | Best practice to avoid re-running |

---

## 🛠️ 3. **Core UI Functions**

| Function                         | Usage                      |
| -------------------------------- | -------------------------- |
| `st.title()`                     | Main title                 |
| `st.header()` / `st.subheader()` | Section headings           |
| `st.text()` / `st.markdown()`    | Plain text & rich text     |
| `st.code()` / `st.latex()`       | Show code blocks, LaTeX    |
| `st.write()`                     | Universal display function |

---

## 🎛️ 4. **Widgets (User Inputs)**

| Widget                                  | Purpose                                        |
| --------------------------------------- | ---------------------------------------------- |
| `st.button()`                           | Trigger actions                                |
| `st.checkbox()`                         | Boolean toggle                                 |
| `st.radio()`                            | Single choice                                  |
| `st.selectbox()` / `st.multiselect()`   | Dropdown menus                                 |
| `st.slider()` / `st.select_slider()`    | Range/Value sliders                            |
| `st.text_input()` / `st.text_area()`    | Text fields                                    |
| `st.number_input()` / `st.date_input()` | Numeric & Date inputs                          |
| `st.file_uploader()`                    | Upload files                                   |
| `st.camera_input()`                     | Capture from camera (new)                      |
| `st.toggle()`                           | Stylish switch (newer alternative to checkbox) |

---

## 📈 5. **Charts & Visualizations**

| Type   | Function                                                |
| ------ | ------------------------------------------------------- |
| Static | `st.line_chart()`, `st.area_chart()`, `st.bar_chart()`  |
| Custom | `st.pyplot()`, `st.altair_chart()`, `st.plotly_chart()` |
| Maps   | `st.map()`, `st.pydeck_chart()`                         |

---

## 📦 6. **Displaying Data**

| Feature   | Function                       |
| --------- | ------------------------------ |
| Tables    | `st.dataframe()`, `st.table()` |
| JSON      | `st.json()`                    |
| Metrics   | `st.metric()` (KPI display)    |
| Columns   | `st.columns()`                 |
| Expanders | `st.expander()`                |

---

## 🔄 7. **State Management**

| Topic          | Feature                                        |
| -------------- | ---------------------------------------------- |
| Session State  | `st.session_state` for saving widget values    |
| Callbacks      | `on_change=` callbacks in widgets              |
| Keying Widgets | Use `key` to prevent re-renders or reuse state |

---

## 🧱 8. **Layout & Containers**

| Feature          | Usage                 |
| ---------------- | --------------------- |
| `st.sidebar`     | Side panel UI         |
| `st.container()` | Custom block          |
| `st.columns()`   | Grid layout           |
| `st.expander()`  | Collapsible section   |
| `st.empty()`     | Placeholder container |

---

## 🧪 9. **File Handling & Media**

| Type     | Function               |
| -------- | ---------------------- |
| Upload   | `st.file_uploader()`   |
| Download | `st.download_button()` |
| Image    | `st.image()`           |
| Audio    | `st.audio()`           |
| Video    | `st.video()`           |

---

## 📤 10. **Interactivity & Callbacks**

| Concept                                 | Use                         |
| --------------------------------------- | --------------------------- |
| `on_click`, `on_change`                 | Bind logic to input changes |
| `st.form()` / `st.form_submit_button()` | Group widget logic          |

---

## 📂 11. **Theming & Appearance**

| Feature                  | Description                 |
| ------------------------ | --------------------------- |
| `.streamlit/config.toml` | Customize default theme     |
| Light/Dark Mode          | UI theming                  |
| `st.set_page_config()`   | Page title, layout, favicon |

---

## ⚙️ 12. **Caching & Performance**

| Function             | Purpose                            |
| -------------------- | ---------------------------------- |
| `@st.cache_data`     | Cache return values (data only)    |
| `@st.cache_resource` | Cache resources like models or DBs |

---

## 📚 13. **Components & Extensions**

| Type                 | Feature                                           |
| -------------------- | ------------------------------------------------- |
| Streamlit Components | `streamlit.components.v1` for embedding HTML/JS   |
| Community Components | e.g., `streamlit-option-menu`, `streamlit-aggrid` |
| Custom Widgets       | via iframe/embed or component SDK                 |

---

## 🔐 14. **Authentication & Deployment (Lightweight)**

| Method      | Usage                                              |
| ----------- | -------------------------------------------------- |
| SSO / OAuth | via Streamlit Community Cloud or external wrappers |
| Deployment  | Streamlit Cloud / HuggingFace / GCP / Docker       |
| Env Vars    | Secure credentials via `st.secrets`                |

---

Great — now that your Streamlit foundation is fully laid out, the next step is to **layer in LangChain and LangGraph integration points**. Here's how we can proceed to ensure it’s comprehensive and smoothly fits into your existing documentation:

---

## 🧠 **15. LangChain & LangGraph Integration**

| Topic                       | Purpose / Usage                                                                   |
| --------------------------- | --------------------------------------------------------------------------------- |
| 📦 Installing & Setting Up  | `pip install langchain langgraph openai` (plus Streamlit & dependencies)          |
| 🧩 Streamlit + LangChain UI | Use widgets (`st.text_input`, `st.button`) to feed LangChain input dynamically    |
| 🔗 Chains & Agents          | Design chains/agents that interact via Streamlit inputs                           |
| 💬 Chatbot UI               | Combine `st.chat_input()` with LangChain conversational agents                    |
| 🧮 Memory Handling          | Persist and manage conversation with `ConversationBufferMemory` + `session_state` |
| 📊 Visualizing Chain Graphs | Use `st.graphviz_chart()` to visualize LangGraph node flows                       |
| 🔁 Callbacks & Tracing      | Integrate LangChain callbacks to Streamlit logs or trace views                    |
| 📁 File / Doc QA            | File upload with `st.file_uploader()` + LangChain loaders & retrieval chains      |
| 🧭 Routing with LangGraph   | Implement node-based workflows (LangGraph) within Streamlit control flows         |
| 🧪 Testing Tools            | Debugging chains and graphs inside `st.expander()` or `st.code()` for trace logs  |
| 🌐 External Tools           | Integrate with tools like OpenAI, Google Search API, SerpAPI, etc.                |
| 🛠️ Agent Toolkits          | Integrate custom tools via LangChain agent tool interfaces                        |
| 📄 YAML / Config Management | Optional YAML chain definitions + upload / parse in Streamlit                     |

---
