---
title: Connection.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4cc4230c7d647d58c0f30bd8351118e6c44198a8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879700"
---
# <a name="connectionclose-method-dao"></a><span data-ttu-id="7957b-102">Connection.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="7957b-102">Connection.Close Method (DAO)</span></span>


<span data-ttu-id="7957b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7957b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7957b-104">Закрывает открытое **подключение**.</span><span class="sxs-lookup"><span data-stu-id="7957b-104">Closes an open **Connection**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7957b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7957b-105">Syntax</span></span>

<span data-ttu-id="7957b-106">*выражение* . Закрыть</span><span class="sxs-lookup"><span data-stu-id="7957b-106">*expression* .Close</span></span>

<span data-ttu-id="7957b-107">*выражение* Переменная, которая содержит объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="7957b-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7957b-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="7957b-108">Remarks</span></span>

<span data-ttu-id="7957b-109">Если при использовании **Close**объекта **набора записей** закрыт, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="7957b-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="7957b-110">При попытке закрыть объект **подключения** имеет все открытые объекты **набора записей** объекты **набора записей** будут закрыты, а все ожидающие обновления или изменения будут отменены.</span><span class="sxs-lookup"><span data-stu-id="7957b-110">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled.</span></span> <span data-ttu-id="7957b-111">Аналогично при попытке закрыть объект **рабочей области** , имеет все открытые объекты **подключения** , эти объекты **подключения** будут закрыты, которой закрывается их объекты **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="7957b-111">Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="7957b-112">Альтернативой метод **Close** — это значение переменной объекта значение **Nothing** (задать dbsTemp = ничего).</span><span class="sxs-lookup"><span data-stu-id="7957b-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

