---
title: Метод Delete (коллекция Fields в ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294108"
---
# <a name="delete-method-ado-fields-collection"></a><span data-ttu-id="4cb4b-102">Метод Delete (коллекция Fields в ADO)</span><span class="sxs-lookup"><span data-stu-id="4cb4b-102">Delete method (ADO Fields Collection)</span></span>

<span data-ttu-id="4cb4b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4cb4b-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="4cb4b-104">Удаляет объект из коллекции [Fields](fields-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="4cb4b-104">Deletes an object from the [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb4b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cb4b-105">Syntax</span></span>

<span data-ttu-id="4cb4b-106">*Поля*. Удаление*поля*</span><span class="sxs-lookup"><span data-stu-id="4cb4b-106">*Fields*.Delete*Field*</span></span>

## <a name="parameters"></a><span data-ttu-id="4cb4b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cb4b-107">Parameters</span></span>

|<span data-ttu-id="4cb4b-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="4cb4b-108">Parameter</span></span>|<span data-ttu-id="4cb4b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4cb4b-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4cb4b-110">*Field*</span><span class="sxs-lookup"><span data-stu-id="4cb4b-110">*Field*</span></span> |<span data-ttu-id="4cb4b-111">**Вариант** , указывающий объект [поля](field-object-ado.md) , который требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="4cb4b-111">A **Variant** that designates the [Field](field-object-ado.md) object to delete.</span></span> <span data-ttu-id="4cb4b-112">Этот параметр может быть именем объекта **field** или порядковым номером самого объекта **field** .</span><span class="sxs-lookup"><span data-stu-id="4cb4b-112">This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.</span></span>|

## <a name="remarks"></a><span data-ttu-id="4cb4b-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="4cb4b-113">Remarks</span></span>

<span data-ttu-id="4cb4b-114">Вызов метода **Fields. Delete** в открытом [наборе записей](recordset-object-ado.md) приводит к ошибке во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="4cb4b-114">Calling the **Fields.Delete** method on an open [Recordset](recordset-object-ado.md) causes a run-time error.</span></span>

