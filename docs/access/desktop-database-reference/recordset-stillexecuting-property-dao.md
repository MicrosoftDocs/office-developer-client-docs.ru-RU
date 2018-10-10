---
title: Recordset.StillExecuting Property (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 0e53c98f-17ac-3569-d780-540a6932013e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845245(v=office.15)
ms:contentKeyID: 48543245
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13a1ca4f3dc0408dbeb26ae56c105d0ee1cf3c6c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481429"
---
# <a name="recordsetstillexecuting-property-dao"></a><span data-ttu-id="edcf9-102">Recordset.StillExecuting Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="edcf9-102">Recordset.StillExecuting Property (DAO)</span></span>


<span data-ttu-id="edcf9-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="edcf9-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="edcf9-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edcf9-104">Syntax</span></span>

<span data-ttu-id="edcf9-105">*выражение* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="edcf9-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="edcf9-106">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="edcf9-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="edcf9-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="edcf9-107">Remarks</span></span>

<span data-ttu-id="edcf9-108">Свойство **StillExecuting** определяет наиболее недавно вызванный асинхронный метод **OpenConnection** (то есть, метод выполнен с помощью параметра **dbRunAsync** ) или **выполнить** завершена.</span><span class="sxs-lookup"><span data-stu-id="edcf9-108">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete.</span></span> <span data-ttu-id="edcf9-109">Хотя свойство **StillExecuting** имеет **значение True**, любой возвращенный объект не были доступны.</span><span class="sxs-lookup"><span data-stu-id="edcf9-109">While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="edcf9-110">Как только свойство **StillExecuting** возвращает **значение False**, следующий за вызовом **OpenConnection** , которое возвращает связанный объект **подключения** можно ссылка на объект.</span><span class="sxs-lookup"><span data-stu-id="edcf9-110">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced.</span></span> <span data-ttu-id="edcf9-111">До тех пор, пока **StillExecuting** остается равным **True**, объект не может существовать ссылок, отличный от для чтения свойство **StillExecuting** .</span><span class="sxs-lookup"><span data-stu-id="edcf9-111">So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="edcf9-112">Используйте метод **[Cancel](connection-cancel-method-dao.md)** для завершения выполнения задачи в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="edcf9-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

