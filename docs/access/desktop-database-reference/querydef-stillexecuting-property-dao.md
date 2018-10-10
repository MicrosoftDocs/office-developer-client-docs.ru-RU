---
title: QueryDef.StillExecuting Property (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 98e85d37-de50-afe1-dcca-01623546e0ad
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197953(v=office.15)
ms:contentKeyID: 48546505
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053584
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b8f3c62795b8e3be65b1f768a3c12092b516593c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481438"
---
# <a name="querydefstillexecuting-property-dao"></a><span data-ttu-id="55160-102">QueryDef.StillExecuting Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="55160-102">QueryDef.StillExecuting Property (DAO)</span></span>


<span data-ttu-id="55160-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="55160-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="55160-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55160-104">Syntax</span></span>

<span data-ttu-id="55160-105">*выражение* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="55160-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="55160-106">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="55160-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="55160-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="55160-107">Remarks</span></span>

<span data-ttu-id="55160-108">Свойство **StillExecuting** определяет наиболее недавно вызванный асинхронный метод **[OpenConnection](dbengine-openconnection-method-dao.md)** (то есть, метод выполнен с помощью параметра **dbRunAsync** ) или **[выполнить](querydef-execute-method-dao.md)** завершена.</span><span class="sxs-lookup"><span data-stu-id="55160-108">Use the **StillExecuting** property to determine if the most recently called asynchronous **[Execute](querydef-execute-method-dao.md)** or **[OpenConnection](dbengine-openconnection-method-dao.md)** method (that is, a method executed with the **dbRunAsync** option) is complete.</span></span> <span data-ttu-id="55160-109">Хотя свойство **StillExecuting** имеет **значение True**, любой возвращенный объект не были доступны.</span><span class="sxs-lookup"><span data-stu-id="55160-109">While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="55160-110">Как только свойство **StillExecuting** возвращает **значение False**, следующий за вызовом **OpenConnection** , которое возвращает связанный объект **[подключения](connection-object-dao.md)** можно ссылка на объект.</span><span class="sxs-lookup"><span data-stu-id="55160-110">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **[Connection](connection-object-dao.md)** object, the object can be referenced.</span></span> <span data-ttu-id="55160-111">До тех пор, пока **StillExecuting** остается равным **True**, объект не может существовать ссылок, отличный от для чтения свойство **StillExecuting** .</span><span class="sxs-lookup"><span data-stu-id="55160-111">So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="55160-112">Используйте метод **[Cancel](connection-cancel-method-dao.md)** для завершения выполнения задачи в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="55160-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

