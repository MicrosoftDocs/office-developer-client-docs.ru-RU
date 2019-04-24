---
title: Метод Recordset2. Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d203d1f1888539a4907da246e20ed711e61ee51f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307415"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="cf1bd-102">Метод Recordset2. Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="cf1bd-102">Recordset2.Cancel method (DAO)</span></span>


<span data-ttu-id="cf1bd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cf1bd-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="cf1bd-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf1bd-104">Syntax</span></span>

<span data-ttu-id="cf1bd-105">*Expression* . Отмена</span><span class="sxs-lookup"><span data-stu-id="cf1bd-105">*expression* .Cancel</span></span>

<span data-ttu-id="cf1bd-106">*Expression (выражение* ) Выражение, возвращающее объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="cf1bd-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf1bd-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="cf1bd-107">Remarks</span></span>

<span data-ttu-id="cf1bd-108">Используйте метод **Cancel** для завершения выполнения асинхронного вызова метода **EXECUTE** или **OpenConnection** (то есть метод вызывается с помощью параметра дбрунасинк).</span><span class="sxs-lookup"><span data-stu-id="cf1bd-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="cf1bd-109">**Отмена** возвращает ошибку времени выполнения, если дбрунасинк не использовался в методе, который вы пытаетесь завершить.</span><span class="sxs-lookup"><span data-stu-id="cf1bd-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

