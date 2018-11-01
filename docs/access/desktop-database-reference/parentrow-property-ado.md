---
title: Свойство ParentRow (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28f0d1c7dbc0e062ff133b9f9997f1a737c3262e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872132"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="ff957-102">Свойство ParentRow (ADO)</span><span class="sxs-lookup"><span data-stu-id="ff957-102">ParentRow property (ADO)</span></span>


<span data-ttu-id="ff957-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff957-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="ff957-104">Задает объект **ADORecordConstruction** контейнер объекта OLE DB **строку** , чтобы родительской строки включается в объект ADO **записи** .</span><span class="sxs-lookup"><span data-stu-id="ff957-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="ff957-105">Только для записи.</span><span class="sxs-lookup"><span data-stu-id="ff957-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff957-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff957-106">Syntax</span></span>

<span data-ttu-id="ff957-107">Поместите HRESULT\_ParentRow (\[в\] IUnknown\* pParent);</span><span class="sxs-lookup"><span data-stu-id="ff957-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="ff957-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff957-108">Parameters</span></span>

  - <span data-ttu-id="ff957-109">*pParent*</span><span class="sxs-lookup"><span data-stu-id="ff957-109">*pParent*</span></span>

  - <span data-ttu-id="ff957-110">Контейнер для строки.</span><span class="sxs-lookup"><span data-stu-id="ff957-110">A container of a row.</span></span>

## <a name="return-values"></a><span data-ttu-id="ff957-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ff957-111">Return values</span></span>

<span data-ttu-id="ff957-112">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="ff957-112">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="ff957-113">Применимо к</span><span class="sxs-lookup"><span data-stu-id="ff957-113">Applies To</span></span>

[<span data-ttu-id="ff957-114">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="ff957-114">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

