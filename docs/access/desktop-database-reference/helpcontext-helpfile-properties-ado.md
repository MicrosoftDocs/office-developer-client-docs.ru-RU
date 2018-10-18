---
<<<<<<< Название HEAD: HelpContext, TOCTitle свойства HelpFile (ADO): HelpContext ms:assetid свойства HelpFile (ADO): 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 09/18 / 2015 mtps_version: v=office.15
---

# <a name="helpcontext-helpfile-properties-ado"></a>HelpContext, HelpFile Properties (ADO)

=== Название: HelpContext свойства HelpFile (ADO) TOCTitle: HelpContext HelpFile свойства (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 10/17/2018 mtps_version: v=office.15
---

# <a name="helpcontext-helpfile-properties-ado"></a>HelpContext свойства HelpFile (ADO)
>>>>>>> master

**Применимо к**: Access 2013 | Office 2013

Указывает файл справки и раздел, связанный с объектом [Ошибка](error-object-ado.md) .

<<<<<<< HEAD
## <a name="return-values"></a>Return Values

  - **HelpContextID** — возвращает идентификатор контекста, как **длинное целое** значение, для раздела в файле справки.

  - **Файл справки** — возвращает **строковое** значение, которое оценивается как полностью разрешенный путь к файлу справки.
=======
## <a name="return-values"></a>Возвращаемые значения

- **HelpContextID** — возвращает идентификатор контекста, как **длинное целое** значение, для раздела в файле справки.

- **Файл справки** — возвращает **строковое** значение, которое оценивается как полностью разрешенный путь к файлу справки.
>>>>>>> master

## <a name="remarks"></a>Замечания

Если в свойство **HelpFile** указан файл справки, свойство **HelpContext** используется для отображения раздела справки, он определяет автоматически. Если нет ни один соответствующий раздел справки, свойство **HelpContext** возвращает нуль и свойство **HelpFile** возвращает строку нулевой длины (»»).

