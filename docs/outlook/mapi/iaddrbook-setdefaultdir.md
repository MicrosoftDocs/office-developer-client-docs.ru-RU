---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3ab01f189734ac30b4c027f4e5596c88031b5f99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341701"
---
# <a name="iaddrbooksetdefaultdir"></a><span data-ttu-id="684c4-103">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="684c4-103">IAddrBook::SetDefaultDir</span></span>

  
  
<span data-ttu-id="684c4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="684c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="684c4-105">Устанавливает указанный контейнер в качестве контейнера адресной книги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="684c4-105">Establishes the specified container as the default address book container.</span></span>
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="684c4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="684c4-106">Parameters</span></span>

 <span data-ttu-id="684c4-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="684c4-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="684c4-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="684c4-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="684c4-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="684c4-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="684c4-110">[in] Указатель на идентификатор записи контейнера адресной книги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="684c4-110">[in] A pointer to the entry identifier of the default address book container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="684c4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="684c4-111">Return value</span></span>

<span data-ttu-id="684c4-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="684c4-112">S_OK</span></span> 
  
> <span data-ttu-id="684c4-113">Контейнер адресной книги по умолчанию был успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="684c4-113">The default address book container was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="684c4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="684c4-114">Remarks</span></span>

<span data-ttu-id="684c4-115">Клиенты и поставщики услуг называют **метод SetDefaultDir** для создания нового контейнера адресной книги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="684c4-115">Clients and service providers call the **SetDefaultDir** method to establish a new default address book container.</span></span> <span data-ttu-id="684c4-116">Контейнер по умолчанию — это контейнер, который пользователь видит в адресной книге при первом открывании адресной книги.</span><span class="sxs-lookup"><span data-stu-id="684c4-116">The default container is the container that the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="684c4-117">**SetDefaultDir** сохраняет контейнер по умолчанию в качестве записи в профиле.</span><span class="sxs-lookup"><span data-stu-id="684c4-117">**SetDefaultDir** saves the default container as an entry in the profile.</span></span> <span data-ttu-id="684c4-118">Контейнер остается по умолчанию до тех пор, пока в том же сеансе или на другом сеансе не будет выполнен другой вызов **в SetDefaultDir** или не будет удален контейнер.</span><span class="sxs-lookup"><span data-stu-id="684c4-118">The container remains as the default until either another call to **SetDefaultDir** is made in the same session or in another session, or the container is removed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="684c4-119">Свойство [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) соответствует параметру **Выберите** автоматически в диалоговом окте "Параметры адресной книги".</span><span class="sxs-lookup"><span data-stu-id="684c4-119">The [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="684c4-120">Если это свойство существует в [разделе IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) профиля и задано значение **true,** диалоговое окно адресной книги больше не по умолчанию подходит для контейнера, указанного **SetDefaultDir,** но выбирает адресную книгу, которую Microsoft Outlook считает подходящей для контекста, в котором диалоговое окно отображалось.</span><span class="sxs-lookup"><span data-stu-id="684c4-120">When this property exists in the [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by **SetDefaultDir**, but chooses an address book that Microsoft Outlook considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="684c4-121">Обратите внимание, что это может привести к плохому опыту сторонних поставщиков адресных книг.</span><span class="sxs-lookup"><span data-stu-id="684c4-121">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="684c4-122">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="684c4-122">MFCMAPI reference</span></span>

<span data-ttu-id="684c4-123">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="684c4-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="684c4-124">**Файл**</span><span class="sxs-lookup"><span data-stu-id="684c4-124">**File**</span></span>|<span data-ttu-id="684c4-125">**Функция**</span><span class="sxs-lookup"><span data-stu-id="684c4-125">**Function**</span></span>|<span data-ttu-id="684c4-126">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="684c4-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="684c4-127">Abcontdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="684c4-127">Abcontdlg.cpp</span></span>  <br/> |<span data-ttu-id="684c4-128">CAbContDlg::OnSetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="684c4-128">CAbContDlg::OnSetDefaultDir</span></span>  <br/> |<span data-ttu-id="684c4-129">MFCMAPI использует метод **SetDefaultDir,** чтобы сделать указанный контейнер адресной книги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="684c4-129">MFCMAPI uses the **SetDefaultDir** method to make the specified address book container the default one.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="684c4-130">См. также</span><span class="sxs-lookup"><span data-stu-id="684c4-130">See also</span></span>



[<span data-ttu-id="684c4-131">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="684c4-131">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="684c4-132">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="684c4-132">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="684c4-133">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="684c4-133">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="684c4-134">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="684c4-134">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="684c4-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="684c4-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="684c4-136">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="684c4-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

