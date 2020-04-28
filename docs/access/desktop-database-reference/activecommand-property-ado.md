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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281931"
---
# <a name="activecommand-property-ado"></a>Свойство ActiveCommand (ADO)

**Область применения**: Access 2013, Office 2013

Указывает объект [Command](command-object-ado.md) , который создал связанный объект [Recordset](recordset-object-ado.md) .

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение типа Variant** , которое содержит объект **Command** . Значение по умолчанию — пустая ссылка на объект.

## <a name="remarks"></a>Примечания

Свойство **ActiveCommand** доступно только для чтения.

Если объект **Command** не использовался для создания текущего объекта **Recordset**, возвращается ссылка на **пустой** объект.

Используйте это свойство, чтобы найти связанный объект **Command** , когда предоставляется только полученный объект **Recordset** .

