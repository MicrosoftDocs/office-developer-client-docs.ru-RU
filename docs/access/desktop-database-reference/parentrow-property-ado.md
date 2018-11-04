---
title: Свойство ParentRow (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06bb1110dfa7e7a055fa6cd863dcd2cc17f3f585
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950154"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="2f16c-102">Свойство ParentRow (ADO)</span><span class="sxs-lookup"><span data-stu-id="2f16c-102">ParentRow property (ADO)</span></span>

<span data-ttu-id="2f16c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f16c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2f16c-104">Задает объект **ADORecordConstruction** контейнер объекта OLE DB **строку** , чтобы родительской строки включается в объект ADO **записи** .</span><span class="sxs-lookup"><span data-stu-id="2f16c-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="2f16c-105">Только для записи.</span><span class="sxs-lookup"><span data-stu-id="2f16c-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f16c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f16c-106">Syntax</span></span>

<span data-ttu-id="2f16c-107">Поместите HRESULT\_ParentRow (\[в\] IUnknown\* pParent);</span><span class="sxs-lookup"><span data-stu-id="2f16c-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="2f16c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f16c-108">Parameters</span></span>

|<span data-ttu-id="2f16c-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="2f16c-109">Parameter</span></span>|<span data-ttu-id="2f16c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="2f16c-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2f16c-111">*pParent*</span><span class="sxs-lookup"><span data-stu-id="2f16c-111">*pParent*</span></span> |<span data-ttu-id="2f16c-112">Контейнер для строки.</span><span class="sxs-lookup"><span data-stu-id="2f16c-112">A container of a row.</span></span>|

## <a name="return-values"></a><span data-ttu-id="2f16c-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2f16c-113">Return values</span></span>

<span data-ttu-id="2f16c-114">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="2f16c-114">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="2f16c-115">Область применения</span><span class="sxs-lookup"><span data-stu-id="2f16c-115">Applies to</span></span>

[<span data-ttu-id="2f16c-116">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="2f16c-116">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

