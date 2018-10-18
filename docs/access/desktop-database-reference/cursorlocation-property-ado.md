---
<<<<<<< Название HEAD: TOCTitle свойство CursorLocation (ADO): свойство CursorLocation (ADO) === название: свойство CursorLocation (ADO) TOCTitle: свойство CursorLocation (ADO)
>>>>>>> главные ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15) ms:contentKeyID: 48546182 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="cursorlocation-property-ado"></a>CursorLocation Property (ADO)
=======
# <a name="cursorlocation-property-ado"></a>Свойство CursorLocation (ADO)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

Указывает расположение службы курсора.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение типа **Long** , может быть установлено одно из значений [CursorLocationEnum](cursorlocationenum.md) .

## <a name="remarks"></a>Замечания

Это свойство можно выбрать одну из различных библиотек курсора, доступной для поставщика. Как правило вы можете выбрать одну с помощью библиотеки курсор на стороне клиента, либо, расположенного на сервере.

Установка этого свойства влияет только после установки свойства подключений. Изменение свойства **CursorLocation** не влияет на существующие подключения.

Курсоры, возвращенный методом [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) наследовать этот параметр. Объекты **набора записей** автоматически наследуют их связанного подключения этот параметр.

Это свойство является чтение и запись на [подключение](connection-object-ado.md) или закрытой [записей](recordset-object-ado.md)и только для чтения на открытие **набора записей**.

**Службы удаленных данных об использовании** При использовании на стороне клиента **записей** или объект **подключения** свойства **CursorLocation** может устанавливаться только для **adUseClient**.

