---
title: Метод Recordset.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 81b08472b46ab3a3d35d184e2f8b7be8673f7d1f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927265"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="ae8c6-102">Метод Recordset.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="ae8c6-102">Recordset.Cancel method (DAO)</span></span>


<span data-ttu-id="ae8c6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae8c6-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="ae8c6-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae8c6-104">Syntax</span></span>

<span data-ttu-id="ae8c6-105">*выражение* . Отмена</span><span class="sxs-lookup"><span data-stu-id="ae8c6-105">*expression* .Cancel</span></span>

<span data-ttu-id="ae8c6-106">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ae8c6-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae8c6-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="ae8c6-107">Remarks</span></span>

<span data-ttu-id="ae8c6-108">Использование метода **Cancel** для завершения выполнения асинхронного вызова метода **Execute** или **OpenConnection** (то есть, метод был вызван с параметром dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="ae8c6-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="ae8c6-109">**Отменить** возвращает ошибку времени выполнения, если в метод, который вы пытаетесь прерывания не используется dbRunAsync.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

