---
title: TableDef.RecordCount Property (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b1d1ab4fee16a9664733c71522cb07a49dde149
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481562"
---
# <a name="tabledefrecordcount-property-dao"></a>TableDef.RecordCount Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Возвращает общее число записей в объекте **[TableDef](tabledef-object-dao.md)** . Только для чтения **времени**.

## <a name="syntax"></a>Синтаксис

*выражение* . RecordCount

*выражение* Переменная, которая представляет собой объект- **TableDef** .

## <a name="remarks"></a>Замечания

Объект **TableDef** или **набора записей** с записи не имеет значение свойства **RecordCount** 0.

При работе с связанных объектов**TableDef** значение свойства **RecordCount** всегда – 1.

