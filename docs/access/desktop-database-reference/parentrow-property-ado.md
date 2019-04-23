---
title: Свойство ParentRow (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2844f7c93164c4b384a895cd32a13bd682154ce3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287740"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="874f9-102">Свойство ParentRow (ADO)</span><span class="sxs-lookup"><span data-stu-id="874f9-102">ParentRow property (ADO)</span></span>

<span data-ttu-id="874f9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="874f9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="874f9-104">Задает контейнер объекта **строки** OLE DB для объекта **ADORecordConstruction** , чтобы родительский элемент строки был включен в объект **записи** ADO.</span><span class="sxs-lookup"><span data-stu-id="874f9-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="874f9-105">Только для записи.</span><span class="sxs-lookup"><span data-stu-id="874f9-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="874f9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="874f9-106">Syntax</span></span>

<span data-ttu-id="874f9-107">HRESULT PUT\_ParentRow (\[в\] IUnknown\* ппарент);</span><span class="sxs-lookup"><span data-stu-id="874f9-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="874f9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="874f9-108">Parameters</span></span>

|<span data-ttu-id="874f9-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="874f9-109">Parameter</span></span>|<span data-ttu-id="874f9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="874f9-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="874f9-111">*Ппарент*</span><span class="sxs-lookup"><span data-stu-id="874f9-111">*pParent*</span></span> |<span data-ttu-id="874f9-112">Контейнер строки.</span><span class="sxs-lookup"><span data-stu-id="874f9-112">A container of a row.</span></span>|

## <a name="return-values"></a><span data-ttu-id="874f9-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="874f9-113">Return values</span></span>

<span data-ttu-id="874f9-114">Этот метод свойства возвращает стандартные значения HRESULT, включая S\_ОК и электронную\_ошибку.</span><span class="sxs-lookup"><span data-stu-id="874f9-114">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="874f9-115">Область применения</span><span class="sxs-lookup"><span data-stu-id="874f9-115">Applies to</span></span>

[<span data-ttu-id="874f9-116">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="874f9-116">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

