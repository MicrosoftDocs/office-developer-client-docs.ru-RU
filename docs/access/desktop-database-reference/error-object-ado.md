---
title: Error Object — ActiveX Data Objects (ADO)
TOCTitle: Error object (ADO)
ms:assetid: 97e478bf-8b25-03a8-9358-abba5069cba3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249678(v=office.15)
ms:contentKeyID: 48546477
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a7c77a59368851f43b5e7bf2275f9f282546fb4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293485"
---
# <a name="error-object-ado"></a>Объект Error (ADO)


**Область применения**: Access 2013, Office 2013

Содержит сведения об ошибках доступа к данным, относящихся к одной операции с участием поставщика.

## <a name="remarks"></a>Заметки

Любая операция, включаемая объекты ADO, может создавать одну или несколько ошибок поставщика. При каждой ошибке один или несколько объектов **Error** помещаются в коллекцию [Errors](errors-collection-ado.md) объекта [Connection.](connection-object-ado.md) Когда другая операция ADO создает ошибку, коллекция **Errors** очищается, а новый набор объектов **Error** помещается в коллекцию **Errors.**

> [!NOTE]
> Каждый **объект Error** представляет определенную ошибку поставщика, а не ошибку ADO. Ошибки ADO оголевются механизмом обработки исключений во время работы. Например, в Microsoft Visual Basic ошибка ADO вызывает событие **On Error** и появляется в **объекте Error.** Полный список ошибок ADO см. в разделе [ErrorValueEnum.](errorvalueenum.md)

Вы можете прочитать свойства **объекта Error,** чтобы получить подробные сведения о каждой ошибке, включая следующие:

- Свойство [Description,](description-property-ado.md) которое содержит текст ошибки. Это свойство по умолчанию.

- Свойство [Number,](number-property-ado.md) которое содержит **длинное** integer значение константы ошибки.

- Свойство [Source,](source-property-ado-error.md) которое идентифицирует объект, который вызывает ошибку. Это особенно полезно, если  после запроса к источнику данных в коллекции errors имеется несколько объектов **Error.**

- Свойства [SQLState](sqlstate-property-ado.md) и [NativeError,](nativeerror-property-ado.md) которые предоставляют сведения из SQL данных.

При ошибке поставщика она помещается в коллекцию **Errors** объекта **Connection.** ADO поддерживает возвращение нескольких ошибок с помощью одной операции ADO, чтобы разрешить сведения об ошибках, характерных для поставщика. Чтобы получить эти сведения об ошибках в обработце ошибок, используйте соответствующие функции перехименовки ошибок языка или среды, с которой вы работаете, а затем используйте вложенные циклы для нумерации свойств каждого объекта **Error** в коллекции **Errors.**

**Пользователи Microsoft Visual Basic и VBScript** Если допустимый объект **Connection** не существует, необходимо получить сведения об ошибке из **объекта Error.**

Как и у поставщиков, ADO очищает объект **OLE Error Info** перед вызовом, который может привести к новой ошибке поставщика. Однако коллекция **Errors** в объекте **Connection** очищается и заполняется только в том случае, если поставщик создает новую ошибку или когда вызывается метод [Clear.](clear-method-ado.md)

Некоторые свойства и методы возвращают предупреждения, которые отображаются как объекты **Error** в коллекции **Errors,** но не останавливают выполнение программы. Перед вызовом [методов Resync,](resync-method-ado.md) [UpdateBatch](updatebatch-method-ado.md)или [CancelBatch](cancelbatch-method-ado.md) для объекта [Recordset;](recordset-object-ado.md) Метод [Open](open-method-ado-connection.md) для объекта **Connection;** или установите свойство [Filter](filter-property-ado.md) для объекта **Recordset,** вызовите метод **Clear** в коллекции **Errors.** Таким образом можно считать свойство [Count](count-property-ado.md) коллекции **Errors** для проверки на возвращенных предупреждений.

