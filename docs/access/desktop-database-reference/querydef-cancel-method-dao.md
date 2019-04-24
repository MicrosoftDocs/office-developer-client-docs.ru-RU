---
title: Метод QueryDef. Cancel (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301122"
---
# <a name="querydefcancel-method-dao"></a><span data-ttu-id="55b9f-102">Метод QueryDef. Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="55b9f-102">QueryDef.Cancel method (DAO)</span></span>


<span data-ttu-id="55b9f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="55b9f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="55b9f-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55b9f-104">Syntax</span></span>

<span data-ttu-id="55b9f-105">*Expression* . Отмена</span><span class="sxs-lookup"><span data-stu-id="55b9f-105">*expression* .Cancel</span></span>

<span data-ttu-id="55b9f-106">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="55b9f-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="55b9f-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="55b9f-107">Remarks</span></span>

<span data-ttu-id="55b9f-108">Используйте метод **Cancel** для завершения выполнения асинхронного вызова метода **EXECUTE** или **OpenConnection** (то есть метод вызывается с помощью параметра дбрунасинк).</span><span class="sxs-lookup"><span data-stu-id="55b9f-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="55b9f-109">**Отмена** возвращает ошибку времени выполнения, если дбрунасинк не использовался в методе, который вы пытаетесь завершить.</span><span class="sxs-lookup"><span data-stu-id="55b9f-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

