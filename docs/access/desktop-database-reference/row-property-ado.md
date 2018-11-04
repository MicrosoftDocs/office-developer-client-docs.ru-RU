---
title: Строка свойство - ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1882486de2a2dfe61b98d4461abeea9cbcc23363
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949315"
---
# <a name="row-property-ado"></a><span data-ttu-id="a483a-102">Свойство Row (ADO)</span><span class="sxs-lookup"><span data-stu-id="a483a-102">Row property (ADO)</span></span>

<span data-ttu-id="a483a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a483a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a483a-104">Получает или задает объект OLE DB **строку** из/на объекте **ADORecordConstruction** .</span><span class="sxs-lookup"><span data-stu-id="a483a-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="a483a-105">При использовании **поместить\_строки** Чтобы установить для объекта **строки** , строка включается в объект ADO **записи** .</span><span class="sxs-lookup"><span data-stu-id="a483a-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="a483a-106">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a483a-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a483a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a483a-107">Syntax</span></span>

<span data-ttu-id="a483a-108">HRESULT get\_строки (\[out retval\] IUnknown\* \* ppRow);</span><span class="sxs-lookup"><span data-stu-id="a483a-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="a483a-109">Поместите HRESULT\_строки (\[в\] IUnknown\* pRow);</span><span class="sxs-lookup"><span data-stu-id="a483a-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="a483a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a483a-110">Parameters</span></span>

|<span data-ttu-id="a483a-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="a483a-111">Parameter</span></span>|<span data-ttu-id="a483a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a483a-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a483a-113">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="a483a-113">*ppRow*</span></span> |<span data-ttu-id="a483a-114">Указатель на объект OLE DB **строки** .</span><span class="sxs-lookup"><span data-stu-id="a483a-114">Pointer to an OLE DB **Row** object.</span></span>|
|<span data-ttu-id="a483a-115">*PRow*</span><span class="sxs-lookup"><span data-stu-id="a483a-115">*PRow*</span></span> |<span data-ttu-id="a483a-116">Объект OLE DB **строки** .</span><span class="sxs-lookup"><span data-stu-id="a483a-116">An OLE DB **Row** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="a483a-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a483a-117">Return values</span></span>

<span data-ttu-id="a483a-118">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="a483a-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a483a-119">Область применения</span><span class="sxs-lookup"><span data-stu-id="a483a-119">Applies to</span></span>

[<span data-ttu-id="a483a-120">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="a483a-120">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

