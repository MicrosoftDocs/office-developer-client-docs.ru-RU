---
title: CALLERRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CALLERRELEASE
api_type:
- HeaderDef
ms.assetid: 80ba893d-3380-4db1-9175-f5b84cb57def
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 69ee06ef8c8f5499dec41232d3dc7b374b15a744
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808124"
---
# <a name="callerrelease"></a><span data-ttu-id="27384-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="27384-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="27384-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27384-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27384-105">Определяет функцию обратного вызова, можно освободить объект данных таблицы при отпускании представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="27384-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27384-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="27384-106">Header file:</span></span>  <br/> |<span data-ttu-id="27384-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="27384-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="27384-108">Функция реализован:</span><span class="sxs-lookup"><span data-stu-id="27384-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="27384-109">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="27384-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="27384-110">Вызывается функция:</span><span class="sxs-lookup"><span data-stu-id="27384-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="27384-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="27384-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="27384-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="27384-112">Parameters</span></span>

 <span data-ttu-id="27384-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="27384-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="27384-114">[in] Данные вызывающего сохраненных с MAPI в табличном представлении и передается **CALLERRELEASE** на основе функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="27384-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="27384-115">Данные предоставляет контекста в табличном представлении освобождения.</span><span class="sxs-lookup"><span data-stu-id="27384-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="27384-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="27384-116">_lpTblData_</span></span>
  
> <span data-ttu-id="27384-117">[in] Указатель на [ITableData: IUnknown](itabledataiunknown.md) интерфейс для основной в табличном представлении освобождения, объект данных таблицы.</span><span class="sxs-lookup"><span data-stu-id="27384-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="27384-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="27384-118">_lpVue_</span></span>
  
> <span data-ttu-id="27384-119">[in] Указатель на [IMAPITable: IUnknown](imapitableiunknown.md) интерфейс для освобождения, представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="27384-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="27384-120">Это интерфейс для объекта в таблице, возвращаемой в параметре _lppMAPITable_ метод [ITableData::HrGetView](itabledata-hrgetview.md) , создавшее этот объект к выпуску.</span><span class="sxs-lookup"><span data-stu-id="27384-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="27384-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="27384-121">Return value</span></span>

<span data-ttu-id="27384-122">Нет</span><span class="sxs-lookup"><span data-stu-id="27384-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="27384-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="27384-123">Remarks</span></span>

<span data-ttu-id="27384-124">Клиентское приложение или поставщика услуг, который заполняется объект данных в таблице можно вызвать [ITableData::HrGetView](itabledata-hrgetview.md) для создания представления только для чтения, отсортированный таблицы.</span><span class="sxs-lookup"><span data-stu-id="27384-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="27384-125">Вызов **HrGetView** передает указатель в функции обратного вызова **CALLERRELEASE** на основе, а также контексте сохранения с в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="27384-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="27384-126">Когда счетчик ссылок в табличном представлении возвращает нулевое значение и выпуска представления, реализация **IMAPITable** вызывает функцию обратного вызова, передав контекста с помощью параметра _ulCallerData_ .</span><span class="sxs-lookup"><span data-stu-id="27384-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="27384-127">Функции обратного вызова **CALLERRELEASE** на основе обычно используется для освобождения базового объекта данных в таблице и имеет для отслеживания его во время последующей обработки.</span><span class="sxs-lookup"><span data-stu-id="27384-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

