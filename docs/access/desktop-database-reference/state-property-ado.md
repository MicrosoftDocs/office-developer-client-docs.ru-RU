---
<<<<<<< Название HEAD: TOCTitle свойство State (ADO): свойство State (ADO) === название: свойством (ADO) состояния TOCTitle: состояний свойство (ADO)
>>>>>>> главные ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15) ms:contentKeyID: 48547053 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:
- ado210.chm1231176 f1_categories:
- Office.Version=v15
---

<<<<<<< HEAD
# <a name="state-property-ado"></a>State Property (ADO)
=======
# <a name="state-property-ado"></a>Свойство состояний (ADO)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

Указывает для всех объектов, которые применяются ли состояние объекта открытой или закрытой.

Указывает, что все соответствующие объекты выполнения асинхронного метода, подключение, выполнение или получение текущего состояния объекта.

<<<<<<< HEAD
## <a name="return-value"></a>Возвращаемое значение
=======
## <a name="return-value"></a>Возвращаемое значение
>>>>>>> master

Возвращает значение типа **Long** , может быть [ObjectStateEnum](objectstateenum.md) значением. Значение по умолчанию — **adStateClosed**.

## <a name="remarks"></a>Замечания

Свойство **состояние** для определения текущего состояния того или иного объекта в любое время.

Свойство **состояние** объекта может содержать комбинацию значений. Например если выполняется оператор, это свойство будет иметь значение объединенный **adStateOpen** и **adStateExecuting**.

Свойство **State** доступен только для чтения.

