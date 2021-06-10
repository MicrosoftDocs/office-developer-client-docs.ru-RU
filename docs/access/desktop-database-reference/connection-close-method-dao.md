---
title: Метод Connection.Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bf99abf97a2eb1b88e7056a36c160eb774959719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295963"
---
# <a name="connectionclose-method-dao"></a><span data-ttu-id="69c48-102">Метод Connection.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="69c48-102">Connection.Close method (DAO)</span></span>


<span data-ttu-id="69c48-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69c48-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69c48-104">Закрывает открытое **подключение.**</span><span class="sxs-lookup"><span data-stu-id="69c48-104">Closes an open **Connection**.</span></span>

## <a name="syntax"></a><span data-ttu-id="69c48-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69c48-105">Syntax</span></span>

<span data-ttu-id="69c48-106">*выражение*.Close</span><span class="sxs-lookup"><span data-stu-id="69c48-106">*expression* .Close</span></span>

<span data-ttu-id="69c48-107">*выражение*: переменная, представляющая объект **Connection**.</span><span class="sxs-lookup"><span data-stu-id="69c48-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="69c48-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="69c48-108">Remarks</span></span>

<span data-ttu-id="69c48-109">Если на момент использования метода **Close** объект **Recordset** уже закрыт, возникнет ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="69c48-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="69c48-110">Если вы попытаетесь закрыть объект **Connection**, у которого имеются какие-либо открытые объекты **Recordset**, объекты **Recordset** будут закрыты, и все ожидающие операции обновления или изменения будут отменены.</span><span class="sxs-lookup"><span data-stu-id="69c48-110">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled.</span></span> <span data-ttu-id="69c48-111">Аналогично, если вы попытаетесь закрыть объект **Workspace**, у которого имеются какие-либо открытые объекты **Connection**, эти объекты **Connection** будут закрыты, что приведет к закрытию их объектов **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="69c48-111">Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="69c48-112">Альтернатива методу **Close** заключается в присвоении объектной переменной значения **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="69c48-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

