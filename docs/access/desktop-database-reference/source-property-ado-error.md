---
title: Свойство Source (Error в ADO)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ae7ea790265edc10be8c907869eefbe4e593ba
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061309"
---
# <a name="source-property-ado-error"></a>Свойство Source (Error в ADO)


**Область применения**: Access 2013, Office 2013

Указывает имя объекта или приложения, которые изначально создали ошибку.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **String,** которое указывает имя объекта или приложения.

## <a name="remarks"></a>Примечания

Используйте свойство **Source** на [объекте Ошибки,](error-object-ado.md) чтобы определить имя объекта или приложения, которые изначально создали ошибку. Это может быть имя класса объекта или программный ID. Для ошибок в ADO значение свойства будет **ADODB.** *ObjectName,* где *ObjectName* — это имя объекта, который вызвал ошибку. Для ADOX и ADO MD значение будет **ADOX.** *ObjectName* и **ADOMD.** *ObjectName соответственно.*

На основе документации об ошибках из свойств **Source,** [Number](number-property-ado.md)и [Description](description-property-ado.md) объектов **Error** можно написать код, который будет соответствующим образом обрабатывать ошибку.

Свойство **Source** — только для чтения для объектов **Error.**

