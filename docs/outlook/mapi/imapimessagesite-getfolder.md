---
title: Имапимессажеситежетфолдер
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
ms.openlocfilehash: 24461099877af683109c8627eacd22a657d6e156
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321387"
---
# <a name="imapimessagesitegetfolder"></a><span data-ttu-id="24162-103">IMAPIMessageSite::GetFolder</span><span class="sxs-lookup"><span data-stu-id="24162-103">IMAPIMessageSite::GetFolder</span></span>

  
  
<span data-ttu-id="24162-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24162-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24162-105">Возвращает папку, в которой было создано или открыто текущее сообщение, если такая папка существует.</span><span class="sxs-lookup"><span data-stu-id="24162-105">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span> <span data-ttu-id="24162-106">Этот метод возвращает значение NULL в параметре _ппфолдер_ для внедренных сообщений, которые не хранятся непосредственно в папке.</span><span class="sxs-lookup"><span data-stu-id="24162-106">This method returns NULL in the  _ppFolder_ parameter for embedded messages, which are not stored directly in a folder.</span></span> 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="24162-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="24162-107">Parameters</span></span>

 <span data-ttu-id="24162-108">_Ппфолдер_</span><span class="sxs-lookup"><span data-stu-id="24162-108">_ppFolder_</span></span>
  
> <span data-ttu-id="24162-109">вышли Указатель на указатель на возвращаемую папку.</span><span class="sxs-lookup"><span data-stu-id="24162-109">[out] A pointer to a pointer to the returned folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="24162-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24162-110">Return value</span></span>

<span data-ttu-id="24162-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="24162-111">S_OK</span></span> 
  
> <span data-ttu-id="24162-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="24162-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="24162-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="24162-113">S_FALSE</span></span> 
  
> <span data-ttu-id="24162-114">Для сообщения не существует папки.</span><span class="sxs-lookup"><span data-stu-id="24162-114">No folder exists for the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="24162-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="24162-115">Remarks</span></span>

<span data-ttu-id="24162-116">Список интерфейсов, связанных с серверами форм, представлен в статье [интерфейсы форм MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="24162-116">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="24162-117">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="24162-117">MFCMAPI reference</span></span>

<span data-ttu-id="24162-118">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="24162-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="24162-119">**Файл**</span><span class="sxs-lookup"><span data-stu-id="24162-119">**File**</span></span>|<span data-ttu-id="24162-120">**Функция**</span><span class="sxs-lookup"><span data-stu-id="24162-120">**Function**</span></span>|<span data-ttu-id="24162-121">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="24162-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="24162-122">Мимапиформвиевер. cpp</span><span class="sxs-lookup"><span data-stu-id="24162-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="24162-123">Кмимапиформвиевер:: @ Folder</span><span class="sxs-lookup"><span data-stu-id="24162-123">CMyMAPIFormViewer::GetFolder</span></span>  <br/> |<span data-ttu-id="24162-124">MFCMAPI использует метод **имапимессажесите::** , чтобы возвратить текущий кэшированный указатель на указанную папку.</span><span class="sxs-lookup"><span data-stu-id="24162-124">MFCMAPI uses the **IMAPIMessageSite::GetFolder** method to return the currently cached pointer to the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24162-125">См. также</span><span class="sxs-lookup"><span data-stu-id="24162-125">See also</span></span>



[<span data-ttu-id="24162-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="24162-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="24162-127">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="24162-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="24162-128">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="24162-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

