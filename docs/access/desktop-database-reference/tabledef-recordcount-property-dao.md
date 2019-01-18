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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722867"
---
# <a name="tabledefrecordcount-property-dao"></a>Свойство TableDef.RecordCount (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает общее число записей в объекте **[TableDef](tabledef-object-dao.md)** . Только для чтения **времени**.

## <a name="syntax"></a>Синтаксис

*выражение* . RecordCount

*выражение* Переменная, которая представляет собой объект- **TableDef** .

## <a name="remarks"></a>Замечания

Объект **TableDef** или **набора записей** с записи не имеет значение свойства **RecordCount** 0.

При работе с связанных объектов**TableDef** значение свойства **RecordCount** всегда – 1.

