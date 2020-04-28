---
title: Свойство Recordset.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 0e53c98f-17ac-3569-d780-540a6932013e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845245(v=office.15)
ms:contentKeyID: 48543245
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1195a45c3846cf79a45c16cda8e23bc95ef8156d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307569"
---
# <a name="recordsetstillexecuting-property-dao"></a><span data-ttu-id="63512-102">Свойство Recordset.StillExecuting (DAO)</span><span class="sxs-lookup"><span data-stu-id="63512-102">Recordset.StillExecuting property (DAO)</span></span>

<span data-ttu-id="63512-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63512-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="63512-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63512-104">Syntax</span></span>

<span data-ttu-id="63512-105">*Expression* . стиллексекутинг</span><span class="sxs-lookup"><span data-stu-id="63512-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="63512-106">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="63512-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="63512-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="63512-107">Remarks</span></span>

<span data-ttu-id="63512-108">Используйте свойство **стиллексекутинг** , чтобы определить, завершен ли последний вызов метода асинхронного **выполнения** или **OpenConnection** (то есть метод, выполняемый с параметром **дбрунасинк** ).</span><span class="sxs-lookup"><span data-stu-id="63512-108">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete.</span></span> <span data-ttu-id="63512-109">Несмотря на то, что свойство **стиллексекутинг** имеет **значение true**, доступ к возвращенному объекту невозможен.</span><span class="sxs-lookup"><span data-stu-id="63512-109">While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="63512-110">После того как свойство **стиллексекутинг** возвращает **значение false**, после вызова **OpenConnection** , возвращающего связанный объект **Connection** , можно ссылаться на объект.</span><span class="sxs-lookup"><span data-stu-id="63512-110">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced.</span></span> <span data-ttu-id="63512-111">До тех пор пока **стиллексекутинг** остается **true**, на объект не может быть ссылок, кроме чтения свойства **стиллексекутинг** .</span><span class="sxs-lookup"><span data-stu-id="63512-111">So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="63512-112">Используйте метод **[Cancel](connection-cancel-method-dao.md)** , чтобы прекратить выполнение задачи в ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="63512-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

