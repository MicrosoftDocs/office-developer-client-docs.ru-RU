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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721726"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="b65a9-102">Свойство ParentRow (ADO)</span><span class="sxs-lookup"><span data-stu-id="b65a9-102">ParentRow property (ADO)</span></span>

<span data-ttu-id="b65a9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b65a9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b65a9-104">Задает объект **ADORecordConstruction** контейнер объекта OLE DB **строку** , чтобы родительской строки включается в объект ADO **записи** .</span><span class="sxs-lookup"><span data-stu-id="b65a9-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="b65a9-105">Только для записи.</span><span class="sxs-lookup"><span data-stu-id="b65a9-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b65a9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b65a9-106">Syntax</span></span>

<span data-ttu-id="b65a9-107">Поместите HRESULT\_ParentRow (\[в\] IUnknown\* pParent);</span><span class="sxs-lookup"><span data-stu-id="b65a9-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="b65a9-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="b65a9-108">Parameters</span></span>

|<span data-ttu-id="b65a9-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="b65a9-109">Parameter</span></span>|<span data-ttu-id="b65a9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b65a9-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b65a9-111">*pParent*</span><span class="sxs-lookup"><span data-stu-id="b65a9-111">*pParent*</span></span> |<span data-ttu-id="b65a9-112">Контейнер для строки.</span><span class="sxs-lookup"><span data-stu-id="b65a9-112">A container of a row.</span></span>|

## <a name="return-values"></a><span data-ttu-id="b65a9-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b65a9-113">Return values</span></span>

<span data-ttu-id="b65a9-114">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="b65a9-114">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b65a9-115">Область применения</span><span class="sxs-lookup"><span data-stu-id="b65a9-115">Applies to</span></span>

[<span data-ttu-id="b65a9-116">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="b65a9-116">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

