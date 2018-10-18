---
<<<<<<< Заголовок HEAD: TOCTitle свойство номер (ADO): свойство номер (ADO) === заголовка: число свойств (ADO) TOCTitle: номер свойство (ADO)
>>>>>>> главные ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15) ms:contentKeyID: 48547243 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="number-property-ado"></a>Number Property (ADO)
=======
# <a name="number-property-ado"></a>Свойство Number (ADO)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

Указывает число, уникально идентифицирующий объект [Error](error-object-ado.md) .

<<<<<<< HEAD
## <a name="return-value"></a>Возвращаемое значение
=======
## <a name="return-value"></a>Возвращаемое значение
>>>>>>> master

Возвращает значение типа **Long** , могут соответствовать одному из константы [ErrorValueEnum](errorvalueenum.md) .

## <a name="remarks"></a>Замечания

Используйте свойство **номер** для определения, какая ошибка произошла. Значение свойства — это уникальное число, соответствующее условия ошибки.

Семейство [Errors](errors-collection-ado.md) возвращает значение HRESULT в шестнадцатеричном формате (например, 0x80004005) или длинное значение (например, 2147467259). Эти значения HRESULT может вызываться базовых компонентах, таких как OLE DB или даже OLE самого. Дополнительные сведения об этих номеров см из *Справочник программиста OLE DB.*

