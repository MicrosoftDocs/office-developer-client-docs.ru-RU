---
title: Source Property (ADO Error)
TOCTitle: Source Property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: adeadcf4c467aabad7b486bd43c12e26d67ce302
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603869"
---
# <a name="source-property-ado-error"></a>Source Property (ADO Error)


**Применимо к**: Access 2013 | Office 2013

Указывает имя объекта или приложения, вызвавшего ошибку.

<<<<<<< HEAD
## <a name="return-value"></a>Возвращаемое значение
=======
## <a name="return-value"></a>Возвращаемое значение
>>>>>>> master

Возвращает **строковое** значение, указывающее имя объекта или приложения.

## <a name="remarks"></a>Замечания

Используйте свойство **Source** на объект [Error](error-object-ado.md) для определения имени объекта или приложения, вызвавшего ошибку. Это может быть имя класса объекта или программный идентификатор. Для ошибок в ADO будет значение свойства **ADODB. *** имя объекта*, где *имя объекта* — это имя объекта, вызвавшей ошибку. Для ADOX и ADO MD значение будет **ADOX. *** имя объекта* и **ADOMD. *** имя объекта,* соответственно.

Основываясь на документацию ошибок из **источника**, [номер](number-property-ado.md)и [Описание](description-property-ado.md) свойств объектов **ошибок** , можно написать код, который будет обрабатывать ошибки соответствующим образом.

Свойство **Source** — только для чтения для объектов **ошибок** .

