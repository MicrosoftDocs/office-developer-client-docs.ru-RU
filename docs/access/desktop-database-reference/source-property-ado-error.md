---
title: Свойство Source (Error в ADO)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f03dcc8049113df13ff8654aee340d1e2d6e502
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308598"
---
# <a name="source-property-ado-error"></a>Свойство Source (Error в ADO)


**Область применения**: Access 2013, Office 2013

Указывает имя объекта или приложения, вызвавшего ошибку.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **строковое** значение, которое указывает имя объекта или приложения.

## <a name="remarks"></a>Замечания

Используйте свойство **Source** для объекта [Error](error-object-ado.md) , чтобы определить имя объекта или приложения, вызвавшего ошибку. Это может быть имя класса объекта или программный идентификатор. Для ошибок в ADO значение свойства равно **ADODB. * * * ObjectName*, где *objectname* — это имя объекта, вызвавшего ошибку. Для ADOX и ADO MD значение будет равно **ADOX. * * * ИмяОбъекта* и **ADOMD. * * * ObjectName,* соответственно.

В соответствии с документацией об ошибках из свойств **Source**, [Number](number-property-ado.md)и [Description](description-property-ado.md) объектов **Error** можно написать код, который будет обрабатывать ошибку соответствующим образом.

Свойство **Source** имеет значение только для чтения для объектов **Error** .

