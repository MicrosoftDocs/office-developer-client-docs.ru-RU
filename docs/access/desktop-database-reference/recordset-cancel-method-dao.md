---
title: Метод Recordset.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 102511575770ceb38cf682d5e627fb7e64faa1ff
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716714"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="c0ca1-102">Метод Recordset.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="c0ca1-102">Recordset.Cancel method (DAO)</span></span>


<span data-ttu-id="c0ca1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0ca1-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ca1-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0ca1-104">Syntax</span></span>

<span data-ttu-id="c0ca1-105">*выражение* . Отмена</span><span class="sxs-lookup"><span data-stu-id="c0ca1-105">*expression* .Cancel</span></span>

<span data-ttu-id="c0ca1-106">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="c0ca1-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0ca1-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="c0ca1-107">Remarks</span></span>

<span data-ttu-id="c0ca1-108">Использование метода **Cancel** для завершения выполнения асинхронного вызова метода **Execute** или **OpenConnection** (то есть, метод был вызван с параметром dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="c0ca1-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="c0ca1-109">**Отменить** возвращает ошибку времени выполнения, если в метод, который вы пытаетесь прерывания не используется dbRunAsync.</span><span class="sxs-lookup"><span data-stu-id="c0ca1-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

