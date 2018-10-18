---
<<<<<<< Название HEAD: TOCTitle свойство LineSeparator (ADO): свойство LineSeparator (ADO) === название: свойство LineSeparator (ADO) TOCTitle: свойство LineSeparator (ADO)
>>>>>>> главные ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15) ms:contentKeyID: 48546676 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="lineseparator-property-ado"></a>LineSeparator Property (ADO)
=======
# <a name="lineseparator-property-ado"></a>Свойство LineSeparator (ADO)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

Указывает двоичных символов для использования в качестве разделителя строки в объектах [потока](stream-object-ado.md) текста.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
=======
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
>>>>>>> master

Задает или возвращает [LineSeparatorsEnum](lineseparatorsenum.md) значение, указывающее знак разделителя строки, используемые в **поток**. Значение по умолчанию — **adCRLF**.

## <a name="remarks"></a>Замечания

**LineSeparator** используется для интерпретации строки при чтении содержимое текста **потока**. С помощью метода [SkipLine](skipline-method-ado.md) можно пропустить строки.

**LineSeparator** используется только с объектами **потока** текста ([Тип](type-property-ado-stream.md) — **adTypeText**). Это свойство игнорируется, если **Тип** — **adTypeBinary**.

