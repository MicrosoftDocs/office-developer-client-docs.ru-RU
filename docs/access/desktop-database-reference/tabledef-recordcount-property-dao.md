---
title: Свойство TableDef.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b24aaa5aec9b17adc169c67733a19a9077a4930
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920923"
---
# <a name="tabledefrecordcount-property-dao"></a>Свойство TableDef.RecordCount (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает общее число записей в объекте **[TableDef](tabledef-object-dao.md)** . Только для чтения **времени**.

## <a name="syntax"></a>Синтаксис

*выражение* . RecordCount

*выражение* Переменная, которая представляет собой объект- **TableDef** .

## <a name="remarks"></a>Примечания

Объект **TableDef** или **набора записей** с записи не имеет значение свойства **RecordCount** 0.

При работе с связанных объектов**TableDef** значение свойства **RecordCount** всегда – 1.

