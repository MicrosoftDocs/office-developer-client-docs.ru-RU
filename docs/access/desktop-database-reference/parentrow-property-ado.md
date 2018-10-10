---
title: ParentRow Property (ADO)
TOCTitle: ParentRow Property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 834dcaed7d1acdcf66410584436e2ccee8c91c56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483248"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="e8fa0-102">ParentRow Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="e8fa0-102">ParentRow Property (ADO)</span></span>


<span data-ttu-id="e8fa0-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8fa0-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="e8fa0-104">Задает объект **ADORecordConstruction** контейнер объекта OLE DB **строку** , чтобы родительской строки включается в объект ADO **записи** .</span><span class="sxs-lookup"><span data-stu-id="e8fa0-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="e8fa0-105">Только для записи.</span><span class="sxs-lookup"><span data-stu-id="e8fa0-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8fa0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8fa0-106">Syntax</span></span>

<span data-ttu-id="e8fa0-107">Поместите HRESULT\_ParentRow (\[в\] IUnknown\* pParent);</span><span class="sxs-lookup"><span data-stu-id="e8fa0-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="e8fa0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8fa0-108">Parameters</span></span>

  - <span data-ttu-id="e8fa0-109">*pParent*</span><span class="sxs-lookup"><span data-stu-id="e8fa0-109">*pParent*</span></span>

  - <span data-ttu-id="e8fa0-110">Контейнер для строки.</span><span class="sxs-lookup"><span data-stu-id="e8fa0-110">A container of a row.</span></span>

## <a name="return-values"></a><span data-ttu-id="e8fa0-111">Return Values</span><span class="sxs-lookup"><span data-stu-id="e8fa0-111">Return Values</span></span>

<span data-ttu-id="e8fa0-112">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="e8fa0-112">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e8fa0-113">Применимо к</span><span class="sxs-lookup"><span data-stu-id="e8fa0-113">Applies To</span></span>

[<span data-ttu-id="e8fa0-114">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="e8fa0-114">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

