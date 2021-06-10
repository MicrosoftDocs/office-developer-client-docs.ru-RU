---
title: Родительское свойство (ADO MD)
TOCTitle: Parent property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0c0eef638cb76676cd2287a34c0e4b17bd89c4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287792"
---
# <a name="parent-property-ado-md"></a>Родительское свойство (ADO MD)


**Область применения**: Access 2013, Office 2013

Указывает участника, который является родителем текущего члена иерархии.

## <a name="return-values"></a>Возвращаемые значения

Возвращает объект [Member](member-object-ado-md.md) и является только для чтения.

## <a name="remarks"></a>Примечания

Член, который находится на верхнем уровне иерархии (корневой) не имеет родительского. Это свойство поддерживается только на **объектах Member,** принадлежащих [объекту Level.](level-object-ado-md.md) Ошибка возникает, когда это свойство ссылается на **объекты Member,** принадлежащие [объекту Position.](position-object-ado-md.md)

