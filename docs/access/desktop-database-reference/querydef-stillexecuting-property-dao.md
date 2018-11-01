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
ms.openlocfilehash: 62290944381687955b19e34f728e9ffff851bcd2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872825"
---
# <a name="querydefstillexecuting-property-dao"></a><span data-ttu-id="6782b-102">QueryDef.StillExecuting Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="6782b-102">QueryDef.StillExecuting Property (DAO)</span></span>


<span data-ttu-id="6782b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6782b-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="6782b-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6782b-104">Syntax</span></span>

<span data-ttu-id="6782b-105">*выражение* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="6782b-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="6782b-106">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="6782b-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6782b-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="6782b-107">Remarks</span></span>

<span data-ttu-id="6782b-108">Свойство **StillExecuting** определяет наиболее недавно вызванный асинхронный метод **[OpenConnection](dbengine-openconnection-method-dao.md)** (то есть, метод выполнен с помощью параметра **dbRunAsync** ) или **[выполнить](querydef-execute-method-dao.md)** завершена.</span><span class="sxs-lookup"><span data-stu-id="6782b-108">Use the **StillExecuting** property to determine if the most recently called asynchronous **[Execute](querydef-execute-method-dao.md)** or **[OpenConnection](dbengine-openconnection-method-dao.md)** method (that is, a method executed with the **dbRunAsync** option) is complete.</span></span> <span data-ttu-id="6782b-109">Хотя свойство **StillExecuting** имеет **значение True**, любой возвращенный объект не были доступны.</span><span class="sxs-lookup"><span data-stu-id="6782b-109">While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="6782b-110">Как только свойство **StillExecuting** возвращает **значение False**, следующий за вызовом **OpenConnection** , которое возвращает связанный объект **[подключения](connection-object-dao.md)** можно ссылка на объект.</span><span class="sxs-lookup"><span data-stu-id="6782b-110">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **[Connection](connection-object-dao.md)** object, the object can be referenced.</span></span> <span data-ttu-id="6782b-111">До тех пор, пока **StillExecuting** остается равным **True**, объект не может существовать ссылок, отличный от для чтения свойство **StillExecuting** .</span><span class="sxs-lookup"><span data-stu-id="6782b-111">So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="6782b-112">Используйте метод **[Cancel](connection-cancel-method-dao.md)** для завершения выполнения задачи в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="6782b-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

