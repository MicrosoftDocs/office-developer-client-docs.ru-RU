---
title: Свойство TableDef.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5eb9588927c9e35fea54964f16150735a7374cd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314289"
---
# <a name="tabledefrecordcount-property-dao"></a>Свойство TableDef.RecordCount (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает общее число записей в **[объекте TableDef.](tabledef-object-dao.md)** Только для чтения, **Long**.

## <a name="syntax"></a>Синтаксис

*выражение* .RecordCount

*выражение*: переменная, представляющая объект **TableDef**.

## <a name="remarks"></a>Комментарии

У объекта **Recordset** или **TableDef** без записей свойству **RecordCount** соответствует значение 0.

При работе со связанными **объектами TableDef** для свойства **RecordCount** всегда задается –1.

