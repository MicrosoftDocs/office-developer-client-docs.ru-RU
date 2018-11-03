---
title: Метод Recordset2.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 159f476b592a8c944df2dc4570d84377c89b5043
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929234"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="425f2-102">Метод Recordset2.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="425f2-102">Recordset2.Cancel method (DAO)</span></span>


<span data-ttu-id="425f2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="425f2-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="425f2-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="425f2-104">Syntax</span></span>

<span data-ttu-id="425f2-105">*выражение* . Отмена</span><span class="sxs-lookup"><span data-stu-id="425f2-105">*expression* .Cancel</span></span>

<span data-ttu-id="425f2-106">*выражение* Выражение, возвращающее объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="425f2-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="425f2-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="425f2-107">Remarks</span></span>

<span data-ttu-id="425f2-108">Использование метода **Cancel** для завершения выполнения асинхронного вызова метода **Execute** или **OpenConnection** (то есть, метод был вызван с параметром dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="425f2-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="425f2-109">**Отменить** возвращает ошибку времени выполнения, если в метод, который вы пытаетесь прерывания не используется dbRunAsync.</span><span class="sxs-lookup"><span data-stu-id="425f2-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

