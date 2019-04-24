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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300814"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="54c61-102">Метод Recordset.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="54c61-102">Recordset.Cancel method (DAO)</span></span>


<span data-ttu-id="54c61-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54c61-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="54c61-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54c61-104">Syntax</span></span>

<span data-ttu-id="54c61-105">*Expression* . Отмена</span><span class="sxs-lookup"><span data-stu-id="54c61-105">*expression* .Cancel</span></span>

<span data-ttu-id="54c61-106">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="54c61-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="54c61-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="54c61-107">Remarks</span></span>

<span data-ttu-id="54c61-108">Используйте метод **Cancel** для завершения выполнения асинхронного вызова метода **EXECUTE** или **OpenConnection** (то есть метод вызывается с помощью параметра дбрунасинк).</span><span class="sxs-lookup"><span data-stu-id="54c61-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="54c61-109">**Отмена** возвращает ошибку времени выполнения, если дбрунасинк не использовался в методе, который вы пытаетесь завершить.</span><span class="sxs-lookup"><span data-stu-id="54c61-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

