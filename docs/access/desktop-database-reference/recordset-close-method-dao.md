---
title: Метод Recordset.Close (DAO)
TOCTitle: Close Method
ms:assetid: e76a81c6-ca0d-e310-c1dc-cbc5d6f6248b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836011(v=office.15)
ms:contentKeyID: 48548404
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5eaa2153e2c420fb91518a47509abec8059d87a0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922848"
---
# <a name="recordsetclose-method-dao"></a><span data-ttu-id="d1fdc-102">Метод Recordset.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="d1fdc-102">Recordset.Close method (DAO)</span></span>


<span data-ttu-id="d1fdc-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d1fdc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d1fdc-104">Закрытие открытых **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="d1fdc-104">Closes an open **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1fdc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1fdc-105">Syntax</span></span>

<span data-ttu-id="d1fdc-106">*выражение* . Закрыть</span><span class="sxs-lookup"><span data-stu-id="d1fdc-106">*expression* .Close</span></span>

<span data-ttu-id="d1fdc-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="d1fdc-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1fdc-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="d1fdc-108">Remarks</span></span>

<span data-ttu-id="d1fdc-109">Если при использовании **Close**объекта **набора записей** закрыт, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="d1fdc-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="d1fdc-110">При попытке закрыть объект **подключения** имеет все открытые объекты **набора записей** объекты **набора записей** будут закрыты, а все ожидающие обновления или изменения будут отменены.</span><span class="sxs-lookup"><span data-stu-id="d1fdc-110">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled.</span></span> <span data-ttu-id="d1fdc-111">Аналогично при попытке закрыть объект **рабочей области** , имеет все открытые объекты **подключения** , эти объекты **подключения** будут закрыты, которой закрывается их объекты **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="d1fdc-111">Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="d1fdc-112">Альтернативой метод **Close** — это значение переменной объекта значение **Nothing** (задать dbsTemp = ничего).</span><span class="sxs-lookup"><span data-stu-id="d1fdc-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

