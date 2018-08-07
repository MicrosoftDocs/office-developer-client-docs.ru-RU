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
ms.openlocfilehash: 00d5b2bfc6b0c024f0ef12ce19fed90ef0af6721
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808756"
---
# <a name="iaddrbooksetdefaultdir"></a><span data-ttu-id="7ea78-103">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="7ea78-103">IAddrBook::SetDefaultDir</span></span>

  
  
<span data-ttu-id="7ea78-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ea78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ea78-105">Устанавливает указанный контейнер как контейнер адресной книги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ea78-105">Establishes the specified container as the default address book container.</span></span>
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="7ea78-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ea78-106">Parameters</span></span>

 <span data-ttu-id="7ea78-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7ea78-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="7ea78-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="7ea78-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="7ea78-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7ea78-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="7ea78-110">[in] Указатель на идентификатор записи контейнер адресной книги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ea78-110">[in] A pointer to the entry identifier of the default address book container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7ea78-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="7ea78-111">Return value</span></span>

<span data-ttu-id="7ea78-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7ea78-112">S_OK</span></span> 
  
> <span data-ttu-id="7ea78-113">Контейнер адресной книги по умолчанию был успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="7ea78-113">The default address book container was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ea78-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="7ea78-114">Remarks</span></span>

<span data-ttu-id="7ea78-115">Клиенты и поставщики услуг вызовите метод **SetDefaultDir** , чтобы установить новый контейнер адресной книги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ea78-115">Clients and service providers call the **SetDefaultDir** method to establish a new default address book container.</span></span> <span data-ttu-id="7ea78-116">Контейнер по умолчанию является контейнером, пользователь видит отображаются в адресной книге, при первом открытии адресной книги.</span><span class="sxs-lookup"><span data-stu-id="7ea78-116">The default container is the container that the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="7ea78-117">**SetDefaultDir** сохраняет контейнер по умолчанию, как запись в профиле.</span><span class="sxs-lookup"><span data-stu-id="7ea78-117">**SetDefaultDir** saves the default container as an entry in the profile.</span></span> <span data-ttu-id="7ea78-118">Контейнер остается по умолчанию, пока другой вызов **SetDefaultDir** выполняется в том же сеансе или в другом сеансе, либо контейнер было удалено.</span><span class="sxs-lookup"><span data-stu-id="7ea78-118">The container remains as the default until either another call to **SetDefaultDir** is made in the same session or in another session, or the container is removed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7ea78-119">Свойство [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) соответствует параметру **автоматически выбирать** в диалоговом окне параметры адресной книги.</span><span class="sxs-lookup"><span data-stu-id="7ea78-119">The [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="7ea78-120">После этого свойства в разделе профилей [IID_CAPONE_PROF](http://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) существует и имеет значение **true**, диалоговое окно адресной книге больше не параметры по умолчанию в контейнер, указанный с **SetDefaultDir**, но выбирает к адресной книге, которая учитывает Microsoft Outlook подходит для контекста, в котором диалоговое окно отображается.</span><span class="sxs-lookup"><span data-stu-id="7ea78-120">When this property exists in the [IID_CAPONE_PROF](http://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by **SetDefaultDir**, but chooses an address book that Microsoft Outlook considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="7ea78-121">Обратите внимание на то, что это может привести к низкого уровня качества для поставщиками сторонних производителей адресной книги.</span><span class="sxs-lookup"><span data-stu-id="7ea78-121">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7ea78-122">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="7ea78-122">MFCMAPI reference</span></span>

<span data-ttu-id="7ea78-123">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="7ea78-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7ea78-124">**����**</span><span class="sxs-lookup"><span data-stu-id="7ea78-124">**File**</span></span>|<span data-ttu-id="7ea78-125">**�������**</span><span class="sxs-lookup"><span data-stu-id="7ea78-125">**Function**</span></span>|<span data-ttu-id="7ea78-126">**�����������**</span><span class="sxs-lookup"><span data-stu-id="7ea78-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7ea78-127">Abcontdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="7ea78-127">Abcontdlg.cpp</span></span>  <br/> |<span data-ttu-id="7ea78-128">CAbContDlg::OnSetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="7ea78-128">CAbContDlg::OnSetDefaultDir</span></span>  <br/> |<span data-ttu-id="7ea78-129">Mfcmapi (en) использует метод **SetDefaultDir** чтобы сделать контейнер указанного адресной книги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ea78-129">MFCMAPI uses the **SetDefaultDir** method to make the specified address book container the default one.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ea78-130">См. также</span><span class="sxs-lookup"><span data-stu-id="7ea78-130">See also</span></span>



[<span data-ttu-id="7ea78-131">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="7ea78-131">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="7ea78-132">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="7ea78-132">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="7ea78-133">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="7ea78-133">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="7ea78-134">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="7ea78-134">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="7ea78-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7ea78-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="7ea78-136">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="7ea78-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

