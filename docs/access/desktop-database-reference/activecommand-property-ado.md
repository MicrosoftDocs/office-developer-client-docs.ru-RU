---
title: ActiveCommand Property (ADO)
TOCTitle: ActiveCommand Property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f01ae4c821d8beb6c8de84c7ed671a373d7372c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482643"
---
# <a name="activecommand-property-ado"></a>ActiveCommand Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает объект [команды](command-object-ado.md) , которые созданы связанного объекта [набора записей](recordset-object-ado.md) .

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **типа Variant** , содержащее объект **команды** . Значение по умолчанию — пустая ссылка на объект.

## <a name="remarks"></a>Замечания

Свойство **ActiveCommand** доступен только для чтения.

Если объект **команды** не использовался для создания текущего **набора записей**, возвращается **значение Null,** ссылки на объект.

Это свойство используется для поиска связанного объекта **команды** , при ей предоставляется только объекте результирующего **набора записей** .

