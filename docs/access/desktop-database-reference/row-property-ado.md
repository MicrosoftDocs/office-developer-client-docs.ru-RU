---
title: Строка свойство - ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715006"
---
# <a name="row-property-ado"></a><span data-ttu-id="d74cc-102">Свойство Row (ADO)</span><span class="sxs-lookup"><span data-stu-id="d74cc-102">Row property (ADO)</span></span>

<span data-ttu-id="d74cc-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d74cc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d74cc-104">Получает или задает объект OLE DB **строку** из/на объекте **ADORecordConstruction** .</span><span class="sxs-lookup"><span data-stu-id="d74cc-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="d74cc-105">При использовании **поместить\_строки** Чтобы установить для объекта **строки** , строка включается в объект ADO **записи** .</span><span class="sxs-lookup"><span data-stu-id="d74cc-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="d74cc-106">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d74cc-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d74cc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d74cc-107">Syntax</span></span>

<span data-ttu-id="d74cc-108">HRESULT get\_строки (\[out retval\] IUnknown\* \* ppRow);</span><span class="sxs-lookup"><span data-stu-id="d74cc-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="d74cc-109">Поместите HRESULT\_строки (\[в\] IUnknown\* pRow);</span><span class="sxs-lookup"><span data-stu-id="d74cc-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="d74cc-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="d74cc-110">Parameters</span></span>

|<span data-ttu-id="d74cc-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="d74cc-111">Parameter</span></span>|<span data-ttu-id="d74cc-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d74cc-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d74cc-113">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="d74cc-113">*ppRow*</span></span> |<span data-ttu-id="d74cc-114">Указатель на объект OLE DB **строки** .</span><span class="sxs-lookup"><span data-stu-id="d74cc-114">Pointer to an OLE DB **Row** object.</span></span>|
|<span data-ttu-id="d74cc-115">*PRow*</span><span class="sxs-lookup"><span data-stu-id="d74cc-115">*PRow*</span></span> |<span data-ttu-id="d74cc-116">Объект OLE DB **строки** .</span><span class="sxs-lookup"><span data-stu-id="d74cc-116">An OLE DB **Row** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="d74cc-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d74cc-117">Return values</span></span>

<span data-ttu-id="d74cc-118">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="d74cc-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="d74cc-119">Область применения</span><span class="sxs-lookup"><span data-stu-id="d74cc-119">Applies to</span></span>

[<span data-ttu-id="d74cc-120">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="d74cc-120">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

