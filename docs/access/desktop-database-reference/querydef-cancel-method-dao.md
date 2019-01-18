---
title: Метод QueryDef.Cancel (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 56a4ba804dba25eb0b4722bcf5396229ee003f43
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720557"
---
# <a name="querydefcancel-method-dao"></a><span data-ttu-id="cd740-102">Метод QueryDef.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="cd740-102">QueryDef.Cancel method (DAO)</span></span>


<span data-ttu-id="cd740-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd740-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="cd740-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd740-104">Syntax</span></span>

<span data-ttu-id="cd740-105">*выражение* . Отмена</span><span class="sxs-lookup"><span data-stu-id="cd740-105">*expression* .Cancel</span></span>

<span data-ttu-id="cd740-106">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="cd740-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd740-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="cd740-107">Remarks</span></span>

<span data-ttu-id="cd740-108">Использование метода **Cancel** для завершения выполнения асинхронного вызова метода **Execute** или **OpenConnection** (то есть, метод был вызван с параметром dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="cd740-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="cd740-109">**Отменить** возвращает ошибку времени выполнения, если в метод, который вы пытаетесь прерывания не используется dbRunAsync.</span><span class="sxs-lookup"><span data-stu-id="cd740-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

