---
title: Recordset.StillExecuting Property (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 0e53c98f-17ac-3569-d780-540a6932013e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845245(v=office.15)
ms:contentKeyID: 48543245
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4c7a245da39f3509022fb0bc4103da88ecbd302a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884375"
---
# <a name="recordsetstillexecuting-property-dao"></a><span data-ttu-id="50193-102">Recordset.StillExecuting Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="50193-102">Recordset.StillExecuting Property (DAO)</span></span>


<span data-ttu-id="50193-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50193-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="50193-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50193-104">Syntax</span></span>

<span data-ttu-id="50193-105">*выражение* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="50193-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="50193-106">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="50193-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="50193-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="50193-107">Remarks</span></span>

<span data-ttu-id="50193-108">Свойство **StillExecuting** определяет наиболее недавно вызванный асинхронный метод **OpenConnection** (то есть, метод выполнен с помощью параметра **dbRunAsync** ) или **выполнить** завершена.</span><span class="sxs-lookup"><span data-stu-id="50193-108">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete.</span></span> <span data-ttu-id="50193-109">Хотя свойство **StillExecuting** имеет **значение True**, любой возвращенный объект не были доступны.</span><span class="sxs-lookup"><span data-stu-id="50193-109">While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="50193-110">Как только свойство **StillExecuting** возвращает **значение False**, следующий за вызовом **OpenConnection** , которое возвращает связанный объект **подключения** можно ссылка на объект.</span><span class="sxs-lookup"><span data-stu-id="50193-110">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced.</span></span> <span data-ttu-id="50193-111">До тех пор, пока **StillExecuting** остается равным **True**, объект не может существовать ссылок, отличный от для чтения свойство **StillExecuting** .</span><span class="sxs-lookup"><span data-stu-id="50193-111">So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="50193-112">Используйте метод **[Cancel](connection-cancel-method-dao.md)** для завершения выполнения задачи в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="50193-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

