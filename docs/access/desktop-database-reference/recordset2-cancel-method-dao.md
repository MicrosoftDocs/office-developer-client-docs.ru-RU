---
title: Метод Recordset2.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d203d1f1888539a4907da246e20ed711e61ee51f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708426"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="7dd67-102">Метод Recordset2.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="7dd67-102">Recordset2.Cancel method (DAO)</span></span>


<span data-ttu-id="7dd67-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7dd67-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="7dd67-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7dd67-104">Syntax</span></span>

<span data-ttu-id="7dd67-105">*выражение* . Отмена</span><span class="sxs-lookup"><span data-stu-id="7dd67-105">*expression* .Cancel</span></span>

<span data-ttu-id="7dd67-106">*выражение* Выражение, возвращающее объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="7dd67-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dd67-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="7dd67-107">Remarks</span></span>

<span data-ttu-id="7dd67-108">Использование метода **Cancel** для завершения выполнения асинхронного вызова метода **Execute** или **OpenConnection** (то есть, метод был вызван с параметром dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="7dd67-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="7dd67-109">**Отменить** возвращает ошибку времени выполнения, если в метод, который вы пытаетесь прерывания не используется dbRunAsync.</span><span class="sxs-lookup"><span data-stu-id="7dd67-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

