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

Указывает имя объекта или приложения, которые изначально создали ошибку.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **строку,** которая указывает имя объекта или приложения.

## <a name="remarks"></a>Заметки

Используйте свойство **Source** объекта [Error,](error-object-ado.md) чтобы определить имя объекта или приложения, которые изначально создали ошибку. Это может быть имя класса или программный ИД объекта. For errors in ADO, the property value will be **ADODB.***ObjectName*, where *ObjectName* is the name of the object that triggered the error. For ADOX and ADO MD, the value will be **ADOX.***ObjectName* and **ADOMD.***ObjectName,* respectively.

На основе документации по ошибке из свойств **Source,** [Number](number-property-ado.md)и [Description](description-property-ado.md) объектов **Error** можно написать код, который будет обрабатывать ошибку соответствующим образом.

Свойство **Source** является "только чтением" для объектов **Error.**

