---
title: Свойство QueryDef.StillExecuting (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 60c0663eaa6857801555c6ce05f4256cfe4c290f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303418"
---
# <a name="querydefstillexecuting-property-dao"></a><span data-ttu-id="ea3e0-102">Свойство QueryDef.StillExecuting (DAO)</span><span class="sxs-lookup"><span data-stu-id="ea3e0-102">QueryDef.StillExecuting property (DAO)</span></span>


<span data-ttu-id="ea3e0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ea3e0-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="ea3e0-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea3e0-104">Syntax</span></span>

<span data-ttu-id="ea3e0-105">*выражения* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="ea3e0-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="ea3e0-106">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="ea3e0-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea3e0-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="ea3e0-107">Remarks</span></span>

<span data-ttu-id="ea3e0-108">Используйте **свойство StillExecuting,** чтобы определить, завершен ли **[](querydef-execute-method-dao.md)** последний метод асинхронного выполнения или **[OpenConnection](dbengine-openconnection-method-dao.md)** (то есть метод, выполненный с помощью параметра **dbRunAsync).**</span><span class="sxs-lookup"><span data-stu-id="ea3e0-108">Use the **StillExecuting** property to determine if the most recently called asynchronous **[Execute](querydef-execute-method-dao.md)** or **[OpenConnection](dbengine-openconnection-method-dao.md)** method (that is, a method executed with the **dbRunAsync** option) is complete.</span></span> <span data-ttu-id="ea3e0-109">Несмотря на то, что свойство **StillExecuting** **является True,** доступ к любому возвращенного объекта невозможно получить.</span><span class="sxs-lookup"><span data-stu-id="ea3e0-109">While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="ea3e0-110">После возвращения **свойства StillExecuting** **False** после вызова **OpenConnection,** **[](connection-object-dao.md)** возвращаемого связанному объекту Подключения, можно ссылаться на объект.</span><span class="sxs-lookup"><span data-stu-id="ea3e0-110">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **[Connection](connection-object-dao.md)** object, the object can be referenced.</span></span> <span data-ttu-id="ea3e0-111">До тех пор, пока **StillExecuting** остается **True,** объект может не ссылаться, кроме как на чтение свойства **StillExecuting.**</span><span class="sxs-lookup"><span data-stu-id="ea3e0-111">So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="ea3e0-112">Чтобы завершить выполнение задачи в процессе выполнения, используйте метод **[Cancel.](connection-cancel-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="ea3e0-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

