# Pharo-Temperature-converter

A graphical temperature converter widget built inside the **Squeak / Smalltalk** environment. This project overrides `BorderedMorph` to create an interactive UI window component that translates Fahrenheit inputs into Celsius while dynamically shifting the window color according to environmental severity.

## 🚀 Features

* **Interactive Morphic UI:** Implements native Smalltalk text inputs (`TextMorph`) and buttons (`SimpleButtonMorph`) packaged into a neat `BorderedMorph` pane layout.
* **Conversion Formula Engine:** Automatically parses and evaluates text entry data strings into a floating-point calculation representing standard Fahrenheit-to-Celsius offsets:
  \[\text{Celsius} = (\text{Fahrenheit} - 32) \times 0.5556\]
* **Dynamic Color Scaling:** The application color shifts in real-time depending on the resulting temperature calculation thresholds:
  * 🥶 **Blue:** Cold temperatures (Result < 5°C)
  * 🌤️ **Light Orange:** Comfortable range (5°C ≤ Result ≤ 21°C)
  * 🥵 **Red:** Hot temperatures (Result > 21°C)

## 🛠️ Tech Stack & Requirements

* **Platform:** [Squeak Smalltalk](https://squeak.org) or [Pharo Object-Oriented IDE Environments](https://pharo.org)
* **Framework:** Morphic Graphical Engine (Built-in standard component)

## 📥 Installation & Environment Integration

1. Open your running **Squeak / Pharo Image**.
2. Open a **System Browser** tool workspace instance.
3. Create a new category named `Assignment-Temp`.
4. Right-click inside the workspace snippet pane area or use your file-in tool to evaluate the raw file contents (`TempMorph.st`) directly to build the class context and methods automatically.

Alternatively, you can evaluate the class schema directly via a **Workspace/Playground** snippet block:

```smalltalk
BorderedMorph subclass: #TempMorph
	instanceVariableNames: 'count countLbl tempInputField'
	classVariableNames: ''
	poolDictionaries: ''
	category: 'Assignment-Temp'
```

## 🎮 How to Run & Use

Once you have initialized the `TempMorph` class and its corresponding method selectors inside your image browser, execute the following small snippet inside a **Workspace** to initialize and view the running visual widget panel component on your screen:

```smalltalk
TempMorph new openInWorld.
```

### Application Step Mapping
1. Click into the input entry box area initialized with the default string placeholder text `'type temp here'`.
2. Input any Fahrenheit numerical coordinate values (e.g., `50`).
3. Click the orange **"Convert"** action selector button.
4. The text view area immediately transforms into the mapped Celsius string reading value, and the background panel tint changes immediately.

## 🗺️ Roadmap & Unfinished Bugs

* [ ] **Fix Initialization Typos:** Remove the unused instantiated local variables (`count`, `countLbl`, `headingLabel`, `cButton`) lingering from base code templates to balance class footprint.
* [ ] **Input Sanitization:** Add validation rules to intercept string text anomalies preventing `asNumber` primitive runtime crashes when filtering unexpected alphanumeric input formats.
* [ ] **Bi-directional Conversion:** Incorporate a toggle setting option switch to support translating metric Celsius values right back into Fahrenheit.

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

