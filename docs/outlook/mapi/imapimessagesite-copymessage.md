---
title: Имапимессажеситекопимессаже
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321548"
---
# <a name="imapimessagesitecopymessage"></a><span data-ttu-id="b64ba-103">IMAPIMessageSite::CopyMessage</span><span class="sxs-lookup"><span data-stu-id="b64ba-103">IMAPIMessageSite::CopyMessage</span></span>

  
  
<span data-ttu-id="b64ba-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b64ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b64ba-105">Копирует текущее сообщение в папку.</span><span class="sxs-lookup"><span data-stu-id="b64ba-105">Copies the current message to a folder.</span></span>
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a><span data-ttu-id="b64ba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b64ba-106">Parameters</span></span>

 <span data-ttu-id="b64ba-107">_Пфолдердестинатион_</span><span class="sxs-lookup"><span data-stu-id="b64ba-107">_pFolderDestination_</span></span>
  
> <span data-ttu-id="b64ba-108">возврата Указатель на папку, в которую необходимо скопировать сообщение.</span><span class="sxs-lookup"><span data-stu-id="b64ba-108">[in] A pointer to the folder where the message is to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b64ba-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b64ba-109">Return value</span></span>

<span data-ttu-id="b64ba-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b64ba-110">S_OK</span></span> 
  
> <span data-ttu-id="b64ba-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="b64ba-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b64ba-112">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="b64ba-112">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b64ba-113">Эта операция не поддерживается этим сайтом сообщений.</span><span class="sxs-lookup"><span data-stu-id="b64ba-113">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b64ba-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b64ba-114">Remarks</span></span>

<span data-ttu-id="b64ba-115">Объекты форм вызовите метод **имапимессажесите:: копимессаже** , чтобы скопировать текущее сообщение в новую папку.</span><span class="sxs-lookup"><span data-stu-id="b64ba-115">Form objects call the **IMAPIMessageSite::CopyMessage** method to copy the current message to a new folder.</span></span> <span data-ttu-id="b64ba-116">**Копимессаже** не изменяет сообщение, отображаемое в данный момент для пользователя, и интерфейс для нового сообщения не возвращается в форму.</span><span class="sxs-lookup"><span data-stu-id="b64ba-116">**CopyMessage** does not change the message currently being displayed to the user, and no interface for the newly created message is returned to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b64ba-117">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="b64ba-117">Notes to implementers</span></span>

<span data-ttu-id="b64ba-118">Типичная реализация метода **копимессаже** выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="b64ba-118">A typical implementation of the **CopyMessage** method performs the following tasks:</span></span> 
  
1. <span data-ttu-id="b64ba-119">Создает новое сообщение для копирования текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="b64ba-119">Creates a new message for the current message to be copied to.</span></span>
    
2. <span data-ttu-id="b64ba-120">Вызывает метод [иперсистмессаже:: Save](ipersistmessage-save.md) с указателем на новое сообщение в параметре _ПМЕССАЖЕ_ и значение false в параметре _фсамеаслоад_ .</span><span class="sxs-lookup"><span data-stu-id="b64ba-120">Calls the [IPersistMessage::Save](ipersistmessage-save.md) method with a pointer to the new message in the  _pMessage_ parameter and FALSE in the  _fSameAsLoad_ parameter.</span></span> 
    
3. <span data-ttu-id="b64ba-121">Вызывает метод [иперсистмессаже:: савекомплетед](ipersistmessage-savecompleted.md) , ПЕРЕДАВАЯ значение NULL в параметре _пмессаже_ .</span><span class="sxs-lookup"><span data-stu-id="b64ba-121">Calls the [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method, passing NULL in the  _pMessage_ parameter.</span></span> 
    
4. <span data-ttu-id="b64ba-122">Вызывает метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) для нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="b64ba-122">Calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the new message.</span></span> 
    
<span data-ttu-id="b64ba-123">Список интерфейсов, связанных с серверами форм, представлен в статье [интерфейсы форм MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="b64ba-123">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b64ba-124">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b64ba-124">MFCMAPI reference</span></span>

<span data-ttu-id="b64ba-125">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b64ba-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b64ba-126">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b64ba-126">**File**</span></span>|<span data-ttu-id="b64ba-127">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b64ba-127">**Function**</span></span>|<span data-ttu-id="b64ba-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="b64ba-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b64ba-129">Мимапиформвиевер. cpp</span><span class="sxs-lookup"><span data-stu-id="b64ba-129">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="b64ba-130">Кмимапиформвиевер:: Копимессаже</span><span class="sxs-lookup"><span data-stu-id="b64ba-130">CMyMAPIFormViewer::CopyMessage</span></span>  <br/> |<span data-ttu-id="b64ba-131">Не реализовано.</span><span class="sxs-lookup"><span data-stu-id="b64ba-131">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b64ba-132">См. также</span><span class="sxs-lookup"><span data-stu-id="b64ba-132">See also</span></span>



[<span data-ttu-id="b64ba-133">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="b64ba-133">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="b64ba-134">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="b64ba-134">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="b64ba-135">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="b64ba-135">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="b64ba-136">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b64ba-136">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="b64ba-137">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="b64ba-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="b64ba-138">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="b64ba-138">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

