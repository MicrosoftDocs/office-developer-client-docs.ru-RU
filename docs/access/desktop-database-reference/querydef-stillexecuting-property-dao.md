---
title: Свойство QueryDef. Стиллексекутинг (DAO)
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
# <a name="querydefstillexecuting-property-dao"></a><span data-ttu-id="0bb8f-102">Свойство QueryDef. Стиллексекутинг (DAO)</span><span class="sxs-lookup"><span data-stu-id="0bb8f-102">QueryDef.StillExecuting property (DAO)</span></span>


<span data-ttu-id="0bb8f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0bb8f-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb8f-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bb8f-104">Syntax</span></span>

<span data-ttu-id="0bb8f-105">*Expression* . Стиллексекутинг</span><span class="sxs-lookup"><span data-stu-id="0bb8f-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="0bb8f-106">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="0bb8f-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bb8f-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="0bb8f-107">Remarks</span></span>

<span data-ttu-id="0bb8f-108">Используйте свойство **стиллексекутинг** , чтобы определить, завершен ли последний вызов метода асинхронного **[выполнения](querydef-execute-method-dao.md)** или **[OpenConnection](dbengine-openconnection-method-dao.md)** (то есть метод, выполняемый с параметром **дбрунасинк** ).</span><span class="sxs-lookup"><span data-stu-id="0bb8f-108">Use the **StillExecuting** property to determine if the most recently called asynchronous **[Execute](querydef-execute-method-dao.md)** or **[OpenConnection](dbengine-openconnection-method-dao.md)** method (that is, a method executed with the **dbRunAsync** option) is complete.</span></span> <span data-ttu-id="0bb8f-109">Несмотря на то, что свойство **стиллексекутинг** имеет **значение true**, доступ к возвращенному объекту невозможен.</span><span class="sxs-lookup"><span data-stu-id="0bb8f-109">While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="0bb8f-110">После того как свойство **стиллексекутинг** возвращает **значение false**, после вызова **OpenConnection** , возвращающего связанный объект **[Connection](connection-object-dao.md)** , можно ссылаться на объект.</span><span class="sxs-lookup"><span data-stu-id="0bb8f-110">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **[Connection](connection-object-dao.md)** object, the object can be referenced.</span></span> <span data-ttu-id="0bb8f-111">До тех пор пока **стиллексекутинг** остается **true**, на объект не может быть ссылок, кроме чтения свойства **стиллексекутинг** .</span><span class="sxs-lookup"><span data-stu-id="0bb8f-111">So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="0bb8f-112">Используйте метод **[Cancel](connection-cancel-method-dao.md)** , чтобы прекратить выполнение задачи в ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="0bb8f-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

