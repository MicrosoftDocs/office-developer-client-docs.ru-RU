---
title: IPersistMessageGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetLastError
api_type:
- COM
ms.assetid: 32cc3a1f-1310-4788-b0f4-93c1e4940f37
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 16f091f4d9527cd82ebc1d1eadee2fb55b481929
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809492"
---
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="2101b-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="2101b-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="2101b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2101b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2101b-105">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущей ошибки в объекте формы.</span><span class="sxs-lookup"><span data-stu-id="2101b-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="2101b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2101b-106">Parameters</span></span>

 <span data-ttu-id="2101b-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="2101b-107">_hResult_</span></span>
  
> <span data-ttu-id="2101b-108">[in] Тип данных HRESULT, которое содержит значение ошибки, созданный в предыдущем вызове метода.</span><span class="sxs-lookup"><span data-stu-id="2101b-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="2101b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2101b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="2101b-110">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="2101b-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="2101b-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="2101b-111">The following flag can be set:</span></span>
    
<span data-ttu-id="2101b-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2101b-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2101b-113">Строки в структуре [MAPIERROR](mapierror.md) , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="2101b-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="2101b-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="2101b-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="2101b-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="2101b-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="2101b-116">[out] Указатель на указатель на структуру **MAPIERROR** , который содержит сведения о версии, компонент и контекста для ошибки.</span><span class="sxs-lookup"><span data-stu-id="2101b-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="2101b-117">Параметр _lppMAPIError_ может быть присвоено значение NULL, если форма не может предоставить соответствующие сведения для структуры **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="2101b-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2101b-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="2101b-118">Return value</span></span>

<span data-ttu-id="2101b-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="2101b-119">S_OK</span></span> 
  
> <span data-ttu-id="2101b-120">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="2101b-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="2101b-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2101b-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2101b-122">Либо был установлен флажок MAPI_UNICODE и поставщик адресной книги не поддерживает Юникод, или MAPI_UNICODE не было установлено и поддерживает только Юникод в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="2101b-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2101b-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="2101b-123">Remarks</span></span>

<span data-ttu-id="2101b-124">Объекты формы реализуйте метод **IPersistMessage::GetLastError** для предоставления сведений о предыдущий вызов, завершившихся сбоем.</span><span class="sxs-lookup"><span data-stu-id="2101b-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="2101b-125">Средства просмотра формы может предоставить их пользователям с подробными сведениями об ошибке, включая данные из структуры [MAPIERROR](mapierror.md) в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="2101b-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="2101b-126">Вызов **GetLastError** не влияет на состояние формы.</span><span class="sxs-lookup"><span data-stu-id="2101b-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="2101b-127">Когда **код последней ошибки** возвращается, форма остается в состоянии, он находился до звонка.</span><span class="sxs-lookup"><span data-stu-id="2101b-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2101b-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="2101b-128">Notes to callers</span></span>

<span data-ttu-id="2101b-129">Структура **MAPIERROR** , можно использовать, если форма предоставляет, который указывает с помощью параметра _lppMAPIError_ только в том случае, если **код последней ошибки** возвращается значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="2101b-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="2101b-130">В некоторых случаях форма не может определить, что последнее сообщение об ошибке была или Дополнительно, чтобы сообщить об ошибке не содержит.</span><span class="sxs-lookup"><span data-stu-id="2101b-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="2101b-131">В этой ситуации форма возвращает указатель на значение NULL в _lppMAPIError_ вместо этого.</span><span class="sxs-lookup"><span data-stu-id="2101b-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="2101b-132">Дополнительные сведения о методе **GetLastError** отображаются [Ошибки расширенного MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="2101b-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2101b-133">См. также</span><span class="sxs-lookup"><span data-stu-id="2101b-133">See also</span></span>



[<span data-ttu-id="2101b-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="2101b-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="2101b-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2101b-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2101b-136">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2101b-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

