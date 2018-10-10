---
title: PageCount Property (ADO)
TOCTitle: PageCount Property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5dcb984cd60d29939a96a7c3b81b17cc825faf46
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482388"
---
# <a name="pagecount-property-ado"></a>PageCount Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Показывает, сколько страниц данных содержит объекта [набора записей](recordset-object-ado.md) .

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа **Long** , показывает, сколько страниц в **набора записей**.

## <a name="remarks"></a>Замечания

Используйте свойство **PageCount** , чтобы определить, сколько страниц данных находятся в объекте **набора записей** . *Страницы* — это группы, размер которого равен значение свойства [PageSize](pagesize-property-ado.md) записей. Даже в том случае, если последней странице не заполнен, так как меньше записей, чем значение **PageSize** , счетчиков на дополнительные в качестве значения **PageCount** . Если объекта **набора записей** не поддерживает это свойство, значение будет равно -1, указывая, что **PageCount** неопределенной.

В разделе свойства **PageSize** и [AbsolutePage](absolutepage-property-ado.md) больше функциональных возможностей на страницу.

