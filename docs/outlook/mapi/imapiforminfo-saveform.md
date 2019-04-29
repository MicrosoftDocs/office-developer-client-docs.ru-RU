---
title: Имапиформинфосавеформ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.SaveForm
api_type:
- COM
ms.assetid: 18a10f14-0795-4d4d-b590-f4cef4f2902a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 391ea3ef4f44db2a9d007241232f58db27647ba2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428748"
---
# <a name="imapiforminfosaveform"></a><span data-ttu-id="423ff-103">IMAPIFormInfo::SaveForm</span><span class="sxs-lookup"><span data-stu-id="423ff-103">IMAPIFormInfo::SaveForm</span></span>

  
  
<span data-ttu-id="423ff-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="423ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="423ff-105">Сохраняет описание конкретной формы в файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="423ff-105">Saves a description of a particular form in a configuration file.</span></span>
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a><span data-ttu-id="423ff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="423ff-106">Parameters</span></span>

 <span data-ttu-id="423ff-107">_Сзфиленаме_</span><span class="sxs-lookup"><span data-stu-id="423ff-107">_szFileName_</span></span>
  
> <span data-ttu-id="423ff-108">возврата Строка с именем файла сообщения Description формы, в котором сохраняется его описание.</span><span class="sxs-lookup"><span data-stu-id="423ff-108">[in] A string that names the form's description message file where its description is saved.</span></span> <span data-ttu-id="423ff-109">Это имя файла должно иметь расширение ФДМ.</span><span class="sxs-lookup"><span data-stu-id="423ff-109">This file name must have the .fdm extension.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="423ff-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="423ff-110">Return value</span></span>

<span data-ttu-id="423ff-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="423ff-111">S_OK</span></span> 
  
> <span data-ttu-id="423ff-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="423ff-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="423ff-113">МАПИ_Е_ЕКСТЕНДЕД_ЕРРОР</span><span class="sxs-lookup"><span data-stu-id="423ff-113">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="423ff-114">Не удалось записать файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="423ff-114">The configuration file could not be written.</span></span> <span data-ttu-id="423ff-115">Чтобы получить структуру [мапиеррор](mapierror.md) , связанную с ошибкой, вызовите метод [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="423ff-115">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="423ff-116">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="423ff-116">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="423ff-117">**Савеформ** , вероятно, был вызван для сохранения формы в локальном контейнере форм.</span><span class="sxs-lookup"><span data-stu-id="423ff-117">**SaveForm** was probably called to save a form in the local form container.</span></span> <span data-ttu-id="423ff-118">**Савеформ** не поддерживается в локальном контейнере форм.</span><span class="sxs-lookup"><span data-stu-id="423ff-118">**SaveForm** is not supported on the local form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="423ff-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="423ff-119">Remarks</span></span>

<span data-ttu-id="423ff-120">Клиентские приложения вызывают метод **имапиформинфо:: савеформ** для сохранения описания текущей формы в файле с заданное именем файла.</span><span class="sxs-lookup"><span data-stu-id="423ff-120">Client applications call the **IMAPIFormInfo::SaveForm** method to save a description of the current form in the file that has the given file name.</span></span> <span data-ttu-id="423ff-121">**Савеформ** создает файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="423ff-121">**SaveForm** creates a configuration file.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="423ff-122">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="423ff-122">Notes to callers</span></span>

<span data-ttu-id="423ff-123">Можно переустановить формы, выбрав их в списке сообщений с дескриптором формы в диалоговом окне, в котором отображаются поставщики библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="423ff-123">You can reinstall forms by selecting them from a list of form descriptor messages in a dialog box that form library providers display.</span></span> <span data-ttu-id="423ff-124">Рекомендуемое расширение для сообщений с дескриптором формы —. ФДМ.</span><span class="sxs-lookup"><span data-stu-id="423ff-124">The recommended extension for form descriptor messages is .fdm.</span></span>
  
<span data-ttu-id="423ff-125">ВыЗовите метод [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) , если **савеформ** возвращает мапи_е_екстендед_еррор, и Проверьте возвращаемую структуру **мапиеррор** , чтобы определить условие, вызвавшее ошибку.</span><span class="sxs-lookup"><span data-stu-id="423ff-125">Call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if **SaveForm** returns MAPI_E_EXTENDED_ERROR, and check the returned **MAPIERROR** structure to determine the condition that caused the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="423ff-126">См. также</span><span class="sxs-lookup"><span data-stu-id="423ff-126">See also</span></span>



[<span data-ttu-id="423ff-127">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="423ff-127">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="423ff-128">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="423ff-128">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="423ff-129">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="423ff-129">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

