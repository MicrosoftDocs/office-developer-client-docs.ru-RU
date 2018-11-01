---
title: Свойство Source (ошибка ADO)
TOCTitle: Source Property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd8a2df4462d9f877d1b4451744fc51215227153
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875107"
---
# <a name="source-property-ado-error"></a>Свойство Source (ошибка ADO)


**Применимо к**: Access 2013, Office 2013

Указывает имя объекта или приложения, вызвавшего ошибку.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **строковое** значение, указывающее имя объекта или приложения.

## <a name="remarks"></a>Замечания

Используйте свойство **Source** на объект [Error](error-object-ado.md) для определения имени объекта или приложения, вызвавшего ошибку. Это может быть имя класса объекта или программный идентификатор. Для ошибок в ADO будет значение свойства **ADODB. *** имя объекта*, где *имя объекта* — это имя объекта, вызвавшей ошибку. Для ADOX и ADO MD значение будет **ADOX. *** имя объекта* и **ADOMD. *** имя объекта,* соответственно.

Основываясь на документацию ошибок из **источника**, [номер](number-property-ado.md)и [Описание](description-property-ado.md) свойств объектов **ошибок** , можно написать код, который будет обрабатывать ошибки соответствующим образом.

Свойство **Source** — только для чтения для объектов **ошибок** .

