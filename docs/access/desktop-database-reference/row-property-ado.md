---
title: Строка свойство - ActiveX Data Objects (ADO)
TOCTitle: Row Property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 05d97bb411c4199677f512d9412653ca5a4b4fe1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481199"
---
# <a name="row-property-ado"></a><span data-ttu-id="e33a0-102">Row Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="e33a0-102">Row Property (ADO)</span></span>


<span data-ttu-id="e33a0-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e33a0-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="e33a0-104">Получает или задает объект OLE DB **строку** из/на объекте **ADORecordConstruction** .</span><span class="sxs-lookup"><span data-stu-id="e33a0-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="e33a0-105">При использовании **поместить\_строки** Чтобы установить для объекта **строки** , строка включается в объект ADO **записи** .</span><span class="sxs-lookup"><span data-stu-id="e33a0-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="e33a0-106">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e33a0-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e33a0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e33a0-107">Syntax</span></span>

<span data-ttu-id="e33a0-108">HRESULT get\_строки (\[out retval\] IUnknown\* \* ppRow);</span><span class="sxs-lookup"><span data-stu-id="e33a0-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="e33a0-109">Поместите HRESULT\_строки (\[в\] IUnknown\* pRow);</span><span class="sxs-lookup"><span data-stu-id="e33a0-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="e33a0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e33a0-110">Parameters</span></span>

  - <span data-ttu-id="e33a0-111">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="e33a0-111">*ppRow*</span></span>

  - <span data-ttu-id="e33a0-112">Указатель на объект OLE DB **строки** .</span><span class="sxs-lookup"><span data-stu-id="e33a0-112">Pointer to an OLE DB **Row** object.</span></span>

  - <span data-ttu-id="e33a0-113">*PRow*</span><span class="sxs-lookup"><span data-stu-id="e33a0-113">*PRow*</span></span>

  - <span data-ttu-id="e33a0-114">Объект OLE DB **строки** .</span><span class="sxs-lookup"><span data-stu-id="e33a0-114">An OLE DB **Row** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="e33a0-115">Return Values</span><span class="sxs-lookup"><span data-stu-id="e33a0-115">Return Values</span></span>

<span data-ttu-id="e33a0-116">Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.</span><span class="sxs-lookup"><span data-stu-id="e33a0-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e33a0-117">Применимо к</span><span class="sxs-lookup"><span data-stu-id="e33a0-117">Applies To</span></span>

[<span data-ttu-id="e33a0-118">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="e33a0-118">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

