---
title: Свойство Recordset2. Стиллексекутинг (DAO)
TOCTitle: StillExecuting Property
ms:assetid: f051c350-0451-44fe-0e47-b152bae4b481
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836546(v=office.15)
ms:contentKeyID: 48548601
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa94622374990ce48c857e9ad45c3531975bb9a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307219"
---
# <a name="recordset2stillexecuting-property-dao"></a><span data-ttu-id="9e1f5-102">Свойство Recordset2. Стиллексекутинг (DAO)</span><span class="sxs-lookup"><span data-stu-id="9e1f5-102">Recordset2.StillExecuting property (DAO)</span></span>


<span data-ttu-id="9e1f5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e1f5-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="9e1f5-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e1f5-104">Syntax</span></span>

<span data-ttu-id="9e1f5-105">*Expression* . Стиллексекутинг</span><span class="sxs-lookup"><span data-stu-id="9e1f5-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="9e1f5-106">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="9e1f5-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e1f5-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="9e1f5-107">Remarks</span></span>

<span data-ttu-id="9e1f5-108">Используйте свойство **стиллексекутинг** , чтобы определить, завершен ли последний вызов метода асинхронного **выполнения** или **OpenConnection** (то есть метод, выполняемый с параметром **дбрунасинк** ).</span><span class="sxs-lookup"><span data-stu-id="9e1f5-108">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete.</span></span> <span data-ttu-id="9e1f5-109">Несмотря на то, что свойство **стиллексекутинг** имеет **значение true**, доступ к возвращенному объекту невозможен.</span><span class="sxs-lookup"><span data-stu-id="9e1f5-109">While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="9e1f5-110">После того как свойство **стиллексекутинг** возвращает **значение false**, после вызова **OpenConnection** , возвращающего связанный объект **Connection** , можно ссылаться на объект.</span><span class="sxs-lookup"><span data-stu-id="9e1f5-110">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced.</span></span> <span data-ttu-id="9e1f5-111">До тех пор пока **стиллексекутинг** остается **true**, на объект не может быть ссылок, кроме чтения свойства **стиллексекутинг** .</span><span class="sxs-lookup"><span data-stu-id="9e1f5-111">So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="9e1f5-112">Используйте метод **[Cancel](connection-cancel-method-dao.md)** , чтобы прекратить выполнение задачи в ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="9e1f5-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

