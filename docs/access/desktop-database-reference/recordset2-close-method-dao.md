---
title: Recordset2.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: ef816969-9857-37cf-9562-d5c80d2815ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836412(v=office.15)
ms:contentKeyID: 48548584
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62bd5f60ed48e863a5190a19e546d292156f8dac
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888337"
---
# <a name="recordset2close-method-dao"></a><span data-ttu-id="11b4d-102">Recordset2.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="11b4d-102">Recordset2.Close Method (DAO)</span></span>


<span data-ttu-id="11b4d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="11b4d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="11b4d-104">Закрытие открытых **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="11b4d-104">Closes an open **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="11b4d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11b4d-105">Syntax</span></span>

<span data-ttu-id="11b4d-106">*выражение* . Закрыть</span><span class="sxs-lookup"><span data-stu-id="11b4d-106">*expression* .Close</span></span>

<span data-ttu-id="11b4d-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="11b4d-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="11b4d-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="11b4d-108">Remarks</span></span>

<span data-ttu-id="11b4d-109">Если при использовании **Close**объекта **набора записей** закрыт, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="11b4d-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="11b4d-110">При попытке закрыть объект **подключения** имеет все открытые объекты **набора записей** объекты **набора записей** будут закрыты, а все ожидающие обновления или изменения будут отменены.</span><span class="sxs-lookup"><span data-stu-id="11b4d-110">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled.</span></span> <span data-ttu-id="11b4d-111">Аналогично при попытке закрыть объект **рабочей области** , имеет все открытые объекты **подключения** , эти объекты **подключения** будут закрыты, которой закрывается их объекты **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="11b4d-111">Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="11b4d-112">Альтернативой метод **Close** — это значение переменной объекта значение **Nothing** (задать dbsTemp = ничего).</span><span class="sxs-lookup"><span data-stu-id="11b4d-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

