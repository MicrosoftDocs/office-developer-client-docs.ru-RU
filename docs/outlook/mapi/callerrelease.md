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
ms.openlocfilehash: 9a22550e60c9de38236a9f612c7e60f50f18978f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408728"
---
# <a name="callerrelease"></a><span data-ttu-id="6a31a-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="6a31a-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="6a31a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a31a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a31a-105">Определяет функцию вызова, которая может освободить объект данных таблицы при выпуске представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="6a31a-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a31a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6a31a-106">Header file:</span></span>  <br/> |<span data-ttu-id="6a31a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6a31a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6a31a-108">Определяемая функция, реализованная в:</span><span class="sxs-lookup"><span data-stu-id="6a31a-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="6a31a-109">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="6a31a-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="6a31a-110">Определяемая функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="6a31a-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="6a31a-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="6a31a-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="6a31a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a31a-112">Parameters</span></span>

 <span data-ttu-id="6a31a-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="6a31a-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="6a31a-114">[in] Данные вызываемого звонка, сохраненные с помощью MAPI в представлении таблицы и переданные функции вызова на основе **CALLERRELEASE.**</span><span class="sxs-lookup"><span data-stu-id="6a31a-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="6a31a-115">Данные предоставляют контекст о представлении таблицы, которая будет отпущена.</span><span class="sxs-lookup"><span data-stu-id="6a31a-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="6a31a-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="6a31a-116">_lpTblData_</span></span>
  
> <span data-ttu-id="6a31a-117">[in] Указатель на [интерфейс ITableData : интерфейс IUnknown](itabledataiunknown.md) для объекта данных таблицы, который находится в окне выпускаемого представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="6a31a-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="6a31a-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="6a31a-118">_lpVue_</span></span>
  
> <span data-ttu-id="6a31a-119">[in] Указатель на [интерфейс IMAPITable : интерфейс IUnknown](imapitableiunknown.md) для выпуска представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="6a31a-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="6a31a-120">Это интерфейс для объекта таблицы, возвращаемого в  _параметре lppMAPITable_ метода [ITableData::HrGetView,](itabledata-hrgetview.md) который создал объект для освобождения.</span><span class="sxs-lookup"><span data-stu-id="6a31a-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6a31a-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a31a-121">Return value</span></span>

<span data-ttu-id="6a31a-122">Нет</span><span class="sxs-lookup"><span data-stu-id="6a31a-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6a31a-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="6a31a-123">Remarks</span></span>

<span data-ttu-id="6a31a-124">Клиентские приложения или поставщик службы, заполнив объект данных таблицы, могут вызвать [ITableData::HrGetView,](itabledata-hrgetview.md) чтобы создать представление таблицы только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6a31a-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="6a31a-125">Вызов **HrGetView** передает указатель функции вызова на основе **CALLERRELEASE,** а также контекст, который необходимо сохранить в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="6a31a-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="6a31a-126">Когда отсчет представления таблицы возвращается к нулю и представление отпущено, реализация **IMAPITable** вызывает функцию обратного вызова, передавая контекст в _параметре ulCallerData._</span><span class="sxs-lookup"><span data-stu-id="6a31a-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="6a31a-127">Функция callback на основе **CALLERRELEASE** часто используется для освобождения объекта данных таблицы, который не должен отслеживаться во время последующей обработки.</span><span class="sxs-lookup"><span data-stu-id="6a31a-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

