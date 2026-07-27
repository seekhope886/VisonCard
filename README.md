# VisonCard
A lightweight extension
# VisonCard Extension (v21.0)

本擴充元件可在 MIT App Inventor 2 與 Niotron 中，將原生的配置盒（Layout）動態升級為帶有**物理 3D 陰影**與**滑順圓角**的現代感卡片（CardView）。

---

## ℹ️ 元件資訊
* **作者**：luckyh9h
* **版本**：21.0 (2026/07/27)
* **相容性**：Android 5.0+ (API 21+)
* **依賴庫**：無（純原生系統元件，輕量不衝突）

---

## 🎨 屬性說明 (Designer)

| 屬性名稱 | 型態 | 預設值 | 說明 |
| :--- | :--- | :--- | :--- |
| **CardBackgroundColor** | Color | 白色 | 設定卡片容器的背景顏色。 |
| **CornerRadius** | Float | 24.0 | 設定卡片的圓角半徑（像素）。 |
| **ShadowElevation** | Float | 12.0 | 設定物理 3D 陰影高度（數值越大陰影越發散）。 |

---

## 🚀 積木說明 (Blocks)

### ➔ CreateCard
將指定的配置盒佈局一秒封裝升級為高品質卡片。

* **輸入參數**：`layoutComponent` (例如：VerticalArrangement)
* **傳回值**：`Object` (可使用 AI2 全域變數接住此物件)

---

## 💡 使用須知
1. **標準寫法**：請建立一個全域變數，並在 `Screen1.Initialize` 時執行：`set 全域變數 to call VisonCard1.CreateCard`。
2. **陰影保護圈**：元件內建 `setUseCompatPadding(true)`，會自動在卡片四周推開 10~15px 的安全距離。設計時請確保配置盒周圍留有空隙，陰影才不會被螢幕邊緣切斷。
3. **自動防溢裁剪**：元件會強迫裁剪卡片內的所有子元件，確保內部的圖片或按鈕不會刺破精美的圓角邊框。

---

## 📥 安裝與使用

1. 從 [Github 社群論壇] 下載最新的 `visoncard.aix` 檔案。
2. 在 MIT App Inventor 專案中，切換到 **Palette** > **Extension** > **Import extension**。
3. 將 **VisonCard** 元件拖放到 Viewer 中。

---

# 📦 [FREE] VisonCard Extension

A lightweight, high-performance extension for MIT App Inventor 2 and Niotron. This extension dynamically wraps any basic native AI2 `Arrangement` (Layout) inside a real Android system **`CardView`**, instantly rendering perfect **physical 3D shadows** and hardware-level rounded corners without any external heavy dependencies.

---

## ℹ️ Extension Information
* **Version**: 21.0
* **Date Created**: July 27, 2026
* **Author**: luckyh9h
* **Category**: UI / Appearance
* **Minimum Android API Level**: API 21 (Android 5.0+)
* **Dependencies**: None (Uses pure Android system built-in components)

---

## 🎨 Designer Properties 

You can configure these properties directly in the Designer properties panel on the right side of the screen.

| Property Name | Editor Type | Default Value | Description |
| :--- | :--- | :--- | :--- |
| **CardBackgroundColor** | Color | `&HFFFFFFFF` (White) | Sets the solid background color of the card container. |
| **CornerRadius** | Float | `24.0` | Sets the radius of the four corners in pixels. |
| **ShadowElevation** | Float | `12.0` | Sets the height of the physical 3D shadow (higher value means larger, softer shadow blur). |

---

## 🚀 Blocks: Functions 

### 🏷️ CreateCard
Dynamically upgrades a standard AI2 layout layout component into a professional modern UI card view.

* **Method Block**: `call VisonCard1.CreateCard`
* **Parameters**: 
  * `layoutComponent` *(AndroidViewComponent)*: The arrangement layout you want to upgrade (e.g., `VerticalArrangement`, `HorizontalArrangement`).
* **Returns**: *(Object)* - Returns the modified `CardView` instance wrapper. This object is fully compatible with AI2 global variables for memory references.

---

### 🛠️ Step-by-Step Installation
1. Go to the right sidebar of this repository, click on **[Releases]()**, and download the latest version of `com.luckyh9h.visoncard.aix`.
2. Click on **Import extension**, choose the downloaded `.aix` file, and click import.
3. Drag and drop the `VisonCard` component into your Viewer workspace. It will appear at the bottom as a *Non-visible component*.

---

### Sourcing & Downloads

Developer / Contact: [halin / miracle ho] 
Compiled Extension File (.aix): VisonCard.aix (11.9 KB) 
Sample Project File (.aia): ui_ext.aia (59.9 KB) 
Feedback, suggestions, and log reports from your OnDebugLog events are highly welcome below! 

## 💡 How to Use & Best Practices 

### 1. Simple 2-Step Implementation
To prevent UI clipping and overlapping errors, always follow this workflow in your **Blocks Editor**:
1. Create a global variable (e.g., `initialize global myCard to 0`) to hold the returned object securely.
2. In the `Screen1.Initialize` event, call the function: 
   `set global myCard to call VisonCard1.CreateCard(layoutComponent: VerticalArrangement2)`

### 2. Auto-Padding & Margin Guard (⚠️ Crucial for Shadows)
* This extension automatically injects `setUseCompatPadding(true)` to push a **10px to 15px invisible safety boundary** around the card. 
* **Design Recommendation**: Ensure your target layout component's `Height` and `Width` properties are **NOT** forced to stretch tightly against screen edges. Leaving a little extra margin space in the Designer will let the smooth, smokey 3D gradient shadow breathe naturally on the screen.

### 3. Hardware-Level Anti-Overflow Clipping
The underlying engine forces `setPreventCornerOverlap(true)`. Any child components you place inside your arrangement (such as images, labels, or inner layouts) will be instantly clipped inside the card boundaries, preventing sharp square edges from poking through your smooth `CornerRadius`.

---

## 📄 License
This extension is open-source and free to use in personal and commercial AI2 projects. Please retain the author attribution (`luckyh9h`) when sharing or modifying.

