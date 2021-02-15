---
title: Row Property - ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306484"
---
# <a name="row-property-ado"></a><span data-ttu-id="c82d0-102">Свойство Row (ADO)</span><span class="sxs-lookup"><span data-stu-id="c82d0-102">Row property (ADO)</span></span>

<span data-ttu-id="c82d0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c82d0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c82d0-104">Получает или задает объект строки OLE **DB** из/объекта **ADORecordConstruction.**</span><span class="sxs-lookup"><span data-stu-id="c82d0-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="c82d0-105">При использовании **put \_ Row** для набора объекта **Row** строка превращается в объект **записи** ADO.</span><span class="sxs-lookup"><span data-stu-id="c82d0-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="c82d0-106">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c82d0-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c82d0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c82d0-107">Syntax</span></span>

<span data-ttu-id="c82d0-108">HRESULT get \_ Row( \[ out, retval \] IUnknown \* \* ppRow);</span><span class="sxs-lookup"><span data-stu-id="c82d0-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="c82d0-109">HRESULT put \_ Row( \[ in \] IUnknown \* pRow);</span><span class="sxs-lookup"><span data-stu-id="c82d0-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="c82d0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c82d0-110">Parameters</span></span>

|<span data-ttu-id="c82d0-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="c82d0-111">Parameter</span></span>|<span data-ttu-id="c82d0-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c82d0-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c82d0-113">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="c82d0-113">*ppRow*</span></span> |<span data-ttu-id="c82d0-114">Указатель на объект строки OLE **DB.**</span><span class="sxs-lookup"><span data-stu-id="c82d0-114">Pointer to an OLE DB **Row** object.</span></span>|
|<span data-ttu-id="c82d0-115">*PRow*</span><span class="sxs-lookup"><span data-stu-id="c82d0-115">*PRow*</span></span> |<span data-ttu-id="c82d0-116">Объект строки OLE **DB.**</span><span class="sxs-lookup"><span data-stu-id="c82d0-116">An OLE DB **Row** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="c82d0-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c82d0-117">Return values</span></span>

<span data-ttu-id="c82d0-118">Этот метод свойства возвращает стандартные значения HRESULT, включая S \_ OK и E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="c82d0-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c82d0-119">Область применения</span><span class="sxs-lookup"><span data-stu-id="c82d0-119">Applies to</span></span>

[<span data-ttu-id="c82d0-120">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="c82d0-120">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

