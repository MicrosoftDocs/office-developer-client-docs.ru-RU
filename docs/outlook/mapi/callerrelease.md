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
# <a name="callerrelease"></a><span data-ttu-id="dc7b6-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="dc7b6-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="dc7b6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc7b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc7b6-105">Определяет функцию обратного вызова, которая может освободить табличный объект данных при отпускании представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="dc7b6-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc7b6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="dc7b6-106">Header file:</span></span>  <br/> |<span data-ttu-id="dc7b6-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="dc7b6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dc7b6-108">Определенная функция реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="dc7b6-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="dc7b6-109">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="dc7b6-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="dc7b6-110">Определенная функция, вызываемая:</span><span class="sxs-lookup"><span data-stu-id="dc7b6-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="dc7b6-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="dc7b6-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="dc7b6-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc7b6-112">Parameters</span></span>

 <span data-ttu-id="dc7b6-113">_Улкаллердата_</span><span class="sxs-lookup"><span data-stu-id="dc7b6-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="dc7b6-114">возврата Данные вызывающего абонента, сохраняемые MAPI с представлением таблицы и переданные в функцию обратного вызова на основе **каллеррелеасе** .</span><span class="sxs-lookup"><span data-stu-id="dc7b6-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="dc7b6-115">Данные представляют собой контекст выпуска представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="dc7b6-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="dc7b6-116">_Лптблдата_</span><span class="sxs-lookup"><span data-stu-id="dc7b6-116">_lpTblData_</span></span>
  
> <span data-ttu-id="dc7b6-117">возврата Указатель на [итабледата: интерфейс IUnknown](itabledataiunknown.md) для объекта данных таблицы, лежащего выпуску табличного представления.</span><span class="sxs-lookup"><span data-stu-id="dc7b6-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="dc7b6-118">_Лпвуе_</span><span class="sxs-lookup"><span data-stu-id="dc7b6-118">_lpVue_</span></span>
  
> <span data-ttu-id="dc7b6-119">возврата Указатель на метод [IMAPITable: интерфейс IUnknown](imapitableiunknown.md) для выпусков табличного представления.</span><span class="sxs-lookup"><span data-stu-id="dc7b6-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="dc7b6-120">Это интерфейс для объекта Table, возвращаемого в параметре _лппмапитабле_ метода [Итабледата:: хржетвиев](itabledata-hrgetview.md) , который создал объект для освобождения.</span><span class="sxs-lookup"><span data-stu-id="dc7b6-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dc7b6-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc7b6-121">Return value</span></span>

<span data-ttu-id="dc7b6-122">Нет</span><span class="sxs-lookup"><span data-stu-id="dc7b6-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dc7b6-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="dc7b6-123">Remarks</span></span>

<span data-ttu-id="dc7b6-124">Клиентское приложение или поставщик услуг, который заполняет объект данных таблицы, может вызывать [итабледата:: хржетвиев](itabledata-hrgetview.md) для создания представления таблицы, отсортированного только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dc7b6-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="dc7b6-125">При вызове **хржетвиев** передается указатель на функцию обратного вызова на основе **каллеррелеасе** , а также контекст для сохранения в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="dc7b6-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="dc7b6-126">Когда счетчик ссылок в представлении таблицы возвращается к нулю и выпуск представления выдается, реализация **IMAPITable** вызывает функцию обратного вызова, передавая контекст в параметр _улкаллердата_ .</span><span class="sxs-lookup"><span data-stu-id="dc7b6-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="dc7b6-127">Обычно функция обратного вызова на основе **каллеррелеасе** используется для высвобождения базового объекта данных таблицы и не обязательно должна отслеживать его во время последующей обработки.</span><span class="sxs-lookup"><span data-stu-id="dc7b6-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

