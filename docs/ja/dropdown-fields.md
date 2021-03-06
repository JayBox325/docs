# セレクトボックスフィールド

セレクトボックスフィールドは、ドロップダウン形式の入力を提供します。

## 設定

セレクトボックスフィールドの設定は、次の通りです。

* **セレクトボックスのオプション** – フィールドで利用可能なオプションを定義します。オプションの値とラベルを別々に設定したり、デフォルトで選択状態にしておくものを選択できます。

## フィールド

セレクトボックスフィールドでは、フィールド設定で定義されたセレクトボックスのオプションがドロップダウン形式で表示されます。

## テンプレート記法

選択されたオプションの値を次のように出力できます。

```twig
{{ entry.dropdownFieldHandle }}
```

選択されたオプションのラベルを次のように出力できます。

```twig
{{ entry.dropdownFieldHandle.label }}
```

または、選択されたものだけでなく、利用可能なすべてのオプションをループすることもできます。

```twig
<ul>
    {% for option in entry.dropdownFieldHandle.options %}
        <li>{{ option }}</li>
    {% endfor %}
</ul>
```

いずれの場合も、オプションのラベルを出力するには `{{ option.label }}` と記述します。オプションが選択されているかどうかは `option.selected` で知ることができます。

例えば、変数に割り当てるなどフィールドの値を直接出力しない場合、次のように `dropdownFieldHandle.value` を利用する必要があります。

```twig
{% set dropdownValue = entry.dropdownFieldHandle.value %}
```

