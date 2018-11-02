---
title: Метод Database.Close (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c97786db2e909074f1a1e0d81e4af03d34301602
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920685"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="77c10-102">Метод Database.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="77c10-102">Database.Close method (DAO)</span></span>


<span data-ttu-id="77c10-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="77c10-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="77c10-104">Закрывает открыть **базу данных**.</span><span class="sxs-lookup"><span data-stu-id="77c10-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="77c10-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77c10-105">Syntax</span></span>

<span data-ttu-id="77c10-106">*выражение* . Закрыть</span><span class="sxs-lookup"><span data-stu-id="77c10-106">*expression* .Close</span></span>

<span data-ttu-id="77c10-107">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="77c10-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="77c10-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="77c10-108">Remarks</span></span>

<span data-ttu-id="77c10-109">Если объект **базы данных** уже работает при использовании **Закрыть**, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="77c10-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="77c10-110">Альтернативой метод **Close** — это значение переменной объекта значение **Nothing** (задать dbsTemp = ничего).</span><span class="sxs-lookup"><span data-stu-id="77c10-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

