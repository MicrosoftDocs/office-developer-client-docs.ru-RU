---
title: IMAPIFormInfoSaveForm
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
# <a name="imapiforminfosaveform"></a><span data-ttu-id="c6542-103">IMAPIFormInfo::SaveForm</span><span class="sxs-lookup"><span data-stu-id="c6542-103">IMAPIFormInfo::SaveForm</span></span>

  
  
<span data-ttu-id="c6542-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6542-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6542-105">Сохраняет описание определенной формы в файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c6542-105">Saves a description of a particular form in a configuration file.</span></span>
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a><span data-ttu-id="c6542-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6542-106">Parameters</span></span>

 <span data-ttu-id="c6542-107">_szFileName_</span><span class="sxs-lookup"><span data-stu-id="c6542-107">_szFileName_</span></span>
  
> <span data-ttu-id="c6542-108">[in] Строка, в которой имя файла сообщения описания формы, в котором сохранено ее описание.</span><span class="sxs-lookup"><span data-stu-id="c6542-108">[in] A string that names the form's description message file where its description is saved.</span></span> <span data-ttu-id="c6542-109">Имя файла должно иметь расширение FDM.</span><span class="sxs-lookup"><span data-stu-id="c6542-109">This file name must have the .fdm extension.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c6542-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6542-110">Return value</span></span>

<span data-ttu-id="c6542-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="c6542-111">S_OK</span></span> 
  
> <span data-ttu-id="c6542-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="c6542-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c6542-113">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="c6542-113">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="c6542-114">Не удалось написать файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c6542-114">The configuration file could not be written.</span></span> <span data-ttu-id="c6542-115">Чтобы получить [структуру MAPIERROR,](mapierror.md) связанную с ошибкой, вызовите метод [IMAPIProp::GetLastError.](imapiprop-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="c6542-115">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="c6542-116">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c6542-116">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c6542-117">Скорее всего, для сохранения формы в локальном контейнере формы был вызван **saveForm.**</span><span class="sxs-lookup"><span data-stu-id="c6542-117">**SaveForm** was probably called to save a form in the local form container.</span></span> <span data-ttu-id="c6542-118">**SaveForm** не поддерживается в локальном контейнере форм.</span><span class="sxs-lookup"><span data-stu-id="c6542-118">**SaveForm** is not supported on the local form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c6542-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="c6542-119">Remarks</span></span>

<span data-ttu-id="c6542-120">Клиентские приложения вызывают метод **IMAPIFormInfo::SaveForm,** чтобы сохранить описание текущей формы в файле с заданным именем файла.</span><span class="sxs-lookup"><span data-stu-id="c6542-120">Client applications call the **IMAPIFormInfo::SaveForm** method to save a description of the current form in the file that has the given file name.</span></span> <span data-ttu-id="c6542-121">**SaveForm** создает файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c6542-121">**SaveForm** creates a configuration file.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c6542-122">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c6542-122">Notes to callers</span></span>

<span data-ttu-id="c6542-123">Можно переустановить формы, выбрав их из списка сообщений дескриптора формы в диалоговом окне, которое отображают поставщики библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="c6542-123">You can reinstall forms by selecting them from a list of form descriptor messages in a dialog box that form library providers display.</span></span> <span data-ttu-id="c6542-124">Рекомендуемое расширение для сообщений дескриптора формы — FDM.</span><span class="sxs-lookup"><span data-stu-id="c6542-124">The recommended extension for form descriptor messages is .fdm.</span></span>
  
<span data-ttu-id="c6542-125">Вызовите метод [IMAPIProp::GetLastError,](imapiprop-getlasterror.md) если **SaveForm** возвращает MAPI_E_EXTENDED_ERROR, и проверьте возвращенную структуру **MAPIERROR,** чтобы определить условие, которое вызвало ошибку.</span><span class="sxs-lookup"><span data-stu-id="c6542-125">Call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if **SaveForm** returns MAPI_E_EXTENDED_ERROR, and check the returned **MAPIERROR** structure to determine the condition that caused the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c6542-126">См. также</span><span class="sxs-lookup"><span data-stu-id="c6542-126">See also</span></span>



[<span data-ttu-id="c6542-127">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c6542-127">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="c6542-128">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="c6542-128">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="c6542-129">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c6542-129">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

