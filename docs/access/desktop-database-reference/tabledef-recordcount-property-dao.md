---
title: TableDef.RecordCount Property (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7ef77f5882f4b215764a82d343d59f1f31487e58
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886118"
---
# <a name="tabledefrecordcount-property-dao"></a>TableDef.RecordCount Property (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает общее число записей в объекте **[TableDef](tabledef-object-dao.md)** . Только для чтения **времени**.

## <a name="syntax"></a>Синтаксис

*выражение* . RecordCount

*выражение* Переменная, которая представляет собой объект- **TableDef** .

## <a name="remarks"></a>Замечания

Объект **TableDef** или **набора записей** с записи не имеет значение свойства **RecordCount** 0.

При работе с связанных объектов**TableDef** значение свойства **RecordCount** всегда – 1.

