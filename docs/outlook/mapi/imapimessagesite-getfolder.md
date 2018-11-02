---
title: IMAPIMessageSiteGetFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFolder
api_type:
- COM
ms.assetid: 9f4b4147-ed98-47cb-a799-ddf028f8e826
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 78fb610c5afc3cac4f6de84240f734e5ae196110
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565545"
---
# <a name="imapimessagesitegetfolder"></a><span data-ttu-id="d73bf-103">IMAPIMessageSite::GetFolder</span><span class="sxs-lookup"><span data-stu-id="d73bf-103">IMAPIMessageSite::GetFolder</span></span>

  
  
<span data-ttu-id="d73bf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d73bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d73bf-105">Возвращает папку, в которой была создана или открыта, текущего сообщения, если такая папка существует.</span><span class="sxs-lookup"><span data-stu-id="d73bf-105">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span> <span data-ttu-id="d73bf-106">Этот метод возвращает значение NULL в параметре _ppFolder_ для внедренных сообщений, которые не хранятся непосредственно в папке.</span><span class="sxs-lookup"><span data-stu-id="d73bf-106">This method returns NULL in the  _ppFolder_ parameter for embedded messages, which are not stored directly in a folder.</span></span> 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="d73bf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d73bf-107">Parameters</span></span>

 <span data-ttu-id="d73bf-108">_ppFolder_</span><span class="sxs-lookup"><span data-stu-id="d73bf-108">_ppFolder_</span></span>
  
> <span data-ttu-id="d73bf-109">[out] Указатель на указатель на папку возвращенные.</span><span class="sxs-lookup"><span data-stu-id="d73bf-109">[out] A pointer to a pointer to the returned folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d73bf-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d73bf-110">Return value</span></span>

<span data-ttu-id="d73bf-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="d73bf-111">S_OK</span></span> 
  
> <span data-ttu-id="d73bf-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="d73bf-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d73bf-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="d73bf-113">S_FALSE</span></span> 
  
> <span data-ttu-id="d73bf-114">Папка не существует в сообщении.</span><span class="sxs-lookup"><span data-stu-id="d73bf-114">No folder exists for the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d73bf-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="d73bf-115">Remarks</span></span>

<span data-ttu-id="d73bf-116">Список интерфейсов, которые связаны с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="d73bf-116">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d73bf-117">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d73bf-117">MFCMAPI reference</span></span>

<span data-ttu-id="d73bf-118">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d73bf-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d73bf-119">**Файл**</span><span class="sxs-lookup"><span data-stu-id="d73bf-119">**File**</span></span>|<span data-ttu-id="d73bf-120">**Функция**</span><span class="sxs-lookup"><span data-stu-id="d73bf-120">**Function**</span></span>|<span data-ttu-id="d73bf-121">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="d73bf-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d73bf-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="d73bf-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="d73bf-123">CMyMAPIFormViewer::GetFolder</span><span class="sxs-lookup"><span data-stu-id="d73bf-123">CMyMAPIFormViewer::GetFolder</span></span>  <br/> |<span data-ttu-id="d73bf-124">Mfcmapi (en) метод **IMAPIMessageSite::GetFolder** возвращает указатель в настоящее время кэширования данных в указанную папку.</span><span class="sxs-lookup"><span data-stu-id="d73bf-124">MFCMAPI uses the **IMAPIMessageSite::GetFolder** method to return the currently cached pointer to the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d73bf-125">См. также</span><span class="sxs-lookup"><span data-stu-id="d73bf-125">See also</span></span>



[<span data-ttu-id="d73bf-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d73bf-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="d73bf-127">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="d73bf-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="d73bf-128">Интерфейсы формы MAPI</span><span class="sxs-lookup"><span data-stu-id="d73bf-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

