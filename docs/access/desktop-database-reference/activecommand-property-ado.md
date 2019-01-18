---
title: Свойство ActiveCommand (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18fa38176f7174f27b46604c6182dfbdaa422f06
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705297"
---
# <a name="activecommand-property-ado"></a>Свойство ActiveCommand (ADO)

**Применимо к**: Access 2013, Office 2013

Указывает объект [команды](command-object-ado.md) , которые созданы связанного объекта [набора записей](recordset-object-ado.md) .

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **типа Variant** , содержащее объект **команды** . Значение по умолчанию — пустая ссылка на объект.

## <a name="remarks"></a>Замечания

Свойство **ActiveCommand** доступен только для чтения.

Если объект **команды** не использовался для создания текущего **набора записей**, возвращается **значение Null,** ссылки на объект.

Это свойство используется для поиска связанного объекта **команды** , при ей предоставляется только объекте результирующего **набора записей** .

