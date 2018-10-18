---
<<<<<<< Название HEAD: TOCTitle свойство атрибуты (ADO): свойство атрибуты (ADO) === название: атрибуты свойства (ADO) TOCTitle: атрибуты свойства (ADO)
>>>>>>> главные ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15) ms:contentKeyID: 48544716 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:
- ado210.chm1231117 f1_categories:
- Office.Version=v15
---

<<<<<<< HEAD
# <a name="attributes-property-ado"></a>Attributes Property (ADO)
=======
# <a name="attributes-property-ado"></a>Свойство Attributes (ADO)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013


## <a name="attributes-property"></a>Свойство Attributes

Указывает один или несколько характеристик объекта.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
=======
## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения
>>>>>>> master

Задает или возвращает значение типа **Long** .

Объект [подключения](connection-object-ado.md) является ли данное свойство **атрибуты** чтения и записи и его значение может быть сумма одно или несколько значений [XactAttributeEnum](xactattributeenum.md) . Значение по умолчанию равно нулю (0).

Свойство **Attributes** — чтение и запись объект [параметра](parameter-object-ado.md) и его значение может быть сумма [ParameterAttributesEnum](parameterattributesenum.md) любого одно или несколько значений. Значение по умолчанию — **adParamSigned**.

Для объекта [поля](field-object-ado.md) свойство **Attributes** может быть сумма одно или несколько значений [FieldAttributeEnum](fieldattributeenum.md) . Обычно только для чтения, однако для новых объектов **полей** , которые добавляются коллекции [полей](fields-collection-ado.md) [записи](record-object-ado.md), **атрибуты** чтения и записи только в том случае, если свойство [Value](value-property-ado.md) для **поля** не указан и новое **поле** успешно добавлена поставщиком данных путем вызова метода [Update](update-method-ado.md) коллекции **полей** .

Для [Свойства](property-object-ado.md) объекта свойство **Attributes** доступен только для чтения и его значение может быть сумма [PropertyAttributesEnum](propertyattributesenum.md) любого одно или несколько значений.

## <a name="remarks"></a>Замечания

Используйте свойство **Attributes** задает или возвращает характеристик объекты **подключения** , объекты **параметров** , объекты [поля](field-object-ado.md) и [Свойства](property-object-ado.md) объектов.

При указании нескольких атрибутов можно суммирования соответствующие константы. Если задать значение свойства для сумм, включая несовместимые константы, возникает ошибка.

**Службы удаленных данных об использовании** Это свойство недоступно на объект **подключения** со стороны клиента.

