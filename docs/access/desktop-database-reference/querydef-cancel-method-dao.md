---
title: QueryDef.Cancel Method (DAO)
TOCTitle: Cancel Method
ms:assetid: 91e61012-c01c-4c24-185c-bdadb7f33a58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197642(v=office.15)
ms:contentKeyID: 48546364
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055470
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8e121457f7084b4d13e89c43a30a7632a3cd7377
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873980"
---
# <a name="querydefcancel-method-dao"></a><span data-ttu-id="8e68d-102">QueryDef.Cancel Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="8e68d-102">QueryDef.Cancel Method (DAO)</span></span>


<span data-ttu-id="8e68d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e68d-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="8e68d-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e68d-104">Syntax</span></span>

<span data-ttu-id="8e68d-105">*выражение* . Отмена</span><span class="sxs-lookup"><span data-stu-id="8e68d-105">*expression* .Cancel</span></span>

<span data-ttu-id="8e68d-106">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="8e68d-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e68d-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="8e68d-107">Remarks</span></span>

<span data-ttu-id="8e68d-108">Использование метода **Cancel** для завершения выполнения асинхронного вызова метода **Execute** или **OpenConnection** (то есть, метод был вызван с параметром dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="8e68d-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="8e68d-109">**Отменить** возвращает ошибку времени выполнения, если в метод, который вы пытаетесь прерывания не используется dbRunAsync.</span><span class="sxs-lookup"><span data-stu-id="8e68d-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

