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
ms.openlocfilehash: ea95ea4efbbf50e5551a27eb81fe5d5ab3b73948
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808956"
---
# <a name="imapimessagesitegetfolder"></a><span data-ttu-id="bd10c-103">IMAPIMessageSite::GetFolder</span><span class="sxs-lookup"><span data-stu-id="bd10c-103">IMAPIMessageSite::GetFolder</span></span>

  
  
<span data-ttu-id="bd10c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd10c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd10c-105">Возвращает папку, в которой была создана или открыта, текущего сообщения, если такая папка существует.</span><span class="sxs-lookup"><span data-stu-id="bd10c-105">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span> <span data-ttu-id="bd10c-106">Этот метод возвращает значение NULL в параметре _ppFolder_ для внедренных сообщений, которые не хранятся непосредственно в папке.</span><span class="sxs-lookup"><span data-stu-id="bd10c-106">This method returns NULL in the  _ppFolder_ parameter for embedded messages, which are not stored directly in a folder.</span></span> 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="bd10c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd10c-107">Parameters</span></span>

 <span data-ttu-id="bd10c-108">_ppFolder_</span><span class="sxs-lookup"><span data-stu-id="bd10c-108">_ppFolder_</span></span>
  
> <span data-ttu-id="bd10c-109">[out] Указатель на указатель на папку возвращенные.</span><span class="sxs-lookup"><span data-stu-id="bd10c-109">[out] A pointer to a pointer to the returned folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bd10c-110">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="bd10c-110">Return value</span></span>

<span data-ttu-id="bd10c-111">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="bd10c-111">S_OK</span></span> 
  
> <span data-ttu-id="bd10c-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="bd10c-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="bd10c-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="bd10c-113">S_FALSE</span></span> 
  
> <span data-ttu-id="bd10c-114">Папка не существует в сообщении.</span><span class="sxs-lookup"><span data-stu-id="bd10c-114">No folder exists for the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bd10c-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="bd10c-115">Remarks</span></span>

<span data-ttu-id="bd10c-116">Список интерфейсов, которые связаны с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="bd10c-116">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bd10c-117">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="bd10c-117">MFCMAPI reference</span></span>

<span data-ttu-id="bd10c-118">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="bd10c-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bd10c-119">**����**</span><span class="sxs-lookup"><span data-stu-id="bd10c-119">**File**</span></span>|<span data-ttu-id="bd10c-120">**�������**</span><span class="sxs-lookup"><span data-stu-id="bd10c-120">**Function**</span></span>|<span data-ttu-id="bd10c-121">**�����������**</span><span class="sxs-lookup"><span data-stu-id="bd10c-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bd10c-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="bd10c-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="bd10c-123">CMyMAPIFormViewer::GetFolder</span><span class="sxs-lookup"><span data-stu-id="bd10c-123">CMyMAPIFormViewer::GetFolder</span></span>  <br/> |<span data-ttu-id="bd10c-124">Mfcmapi (en) метод **IMAPIMessageSite::GetFolder** возвращает указатель в настоящее время кэширования данных в указанную папку.</span><span class="sxs-lookup"><span data-stu-id="bd10c-124">MFCMAPI uses the **IMAPIMessageSite::GetFolder** method to return the currently cached pointer to the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd10c-125">См. также</span><span class="sxs-lookup"><span data-stu-id="bd10c-125">See also</span></span>



[<span data-ttu-id="bd10c-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bd10c-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="bd10c-127">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="bd10c-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="bd10c-128">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="bd10c-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

