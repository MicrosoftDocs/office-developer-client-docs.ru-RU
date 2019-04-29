---
title: Имапифолдеркреатефолдер
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 606d780aa59e363c30ddc7a5b562db64d845ccb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436764"
---
# <a name="imapifoldercreatefolder"></a><span data-ttu-id="9310f-103">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="9310f-103">IMAPIFolder::CreateFolder</span></span>

  
  
<span data-ttu-id="9310f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9310f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9310f-105">Создает новую вложенную папку.</span><span class="sxs-lookup"><span data-stu-id="9310f-105">Creates a new subfolder.</span></span>
  
```cpp
HRESULT CreateFolder(
  ULONG ulFolderType,
  LPSTR lpszFolderName,
  LPSTR lpszFolderComment,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMAPIFOLDER FAR * lppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="9310f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9310f-106">Parameters</span></span>

 <span data-ttu-id="9310f-107">_Улфолдертипе_</span><span class="sxs-lookup"><span data-stu-id="9310f-107">_ulFolderType_</span></span>
  
> <span data-ttu-id="9310f-108">возврата Тип создаваемой папки.</span><span class="sxs-lookup"><span data-stu-id="9310f-108">[in] The type of folder to create.</span></span> <span data-ttu-id="9310f-109">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="9310f-109">The following flags can be set:</span></span>
    
<span data-ttu-id="9310f-110">ФОЛДЕР_ЖЕНЕРИК</span><span class="sxs-lookup"><span data-stu-id="9310f-110">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="9310f-111">Следует создать универсальную папку.</span><span class="sxs-lookup"><span data-stu-id="9310f-111">A generic folder should be created.</span></span>
    
<span data-ttu-id="9310f-112">ФОЛДЕР_СЕАРЧ</span><span class="sxs-lookup"><span data-stu-id="9310f-112">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="9310f-113">Следует создать папку результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="9310f-113">A search-results folder should be created.</span></span>
    
 <span data-ttu-id="9310f-114">_Лпсзфолдернаме_</span><span class="sxs-lookup"><span data-stu-id="9310f-114">_lpszFolderName_</span></span>
  
> <span data-ttu-id="9310f-115">возврата Указатель на строку, содержащую имя новой папки.</span><span class="sxs-lookup"><span data-stu-id="9310f-115">[in] A pointer to a string that contains the name for the new folder.</span></span> <span data-ttu-id="9310f-116">Это имя является основой для свойства **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) новой папки.</span><span class="sxs-lookup"><span data-stu-id="9310f-116">This name is the basis for the new folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="9310f-117">_Лпсзфолдеркоммент_</span><span class="sxs-lookup"><span data-stu-id="9310f-117">_lpszFolderComment_</span></span>
  
> <span data-ttu-id="9310f-118">возврата Указатель на строку, содержащую комментарий, связанный с новой папкой.</span><span class="sxs-lookup"><span data-stu-id="9310f-118">[in] A pointer to a string that contains a comment associated with the new folder.</span></span> <span data-ttu-id="9310f-119">Эта строка становится значением свойства **пр_коммент** ([PidTagComment](pidtagcomment-canonical-property.md)) новой папки.</span><span class="sxs-lookup"><span data-stu-id="9310f-119">This string becomes the value of the new folder's **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) property.</span></span> <span data-ttu-id="9310f-120">Если передается значение NULL, то папка не имеет исходного комментария.</span><span class="sxs-lookup"><span data-stu-id="9310f-120">If NULL is passed, the folder has no initial comment.</span></span>
    
 <span data-ttu-id="9310f-121">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="9310f-121">_lpInterface_</span></span>
  
> <span data-ttu-id="9310f-122">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к новой папке.</span><span class="sxs-lookup"><span data-stu-id="9310f-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new folder.</span></span> <span data-ttu-id="9310f-123">При передаче значения NULL поставщику хранилища сообщений возвращается интерфейс стандартных папок, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="9310f-123">Passing NULL causes the message store provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="9310f-124">Клиенты должны передавать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="9310f-124">Clients must pass NULL.</span></span> <span data-ttu-id="9310f-125">Другие абоненты могут задать для параметра _лпинтерфаце_ значение Иид_иункновн, Иид_имапипроп, Иид_имапиконтаинер или иид_имапифолдер.</span><span class="sxs-lookup"><span data-stu-id="9310f-125">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="9310f-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9310f-126">_ulFlags_</span></span>
  
> <span data-ttu-id="9310f-127">возврата Битовая маска флагов, определяющих способ создания папки.</span><span class="sxs-lookup"><span data-stu-id="9310f-127">[in] A bitmask of flags that controls how the folder is created.</span></span> <span data-ttu-id="9310f-128">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="9310f-128">The following flags can be set:</span></span>
    
<span data-ttu-id="9310f-129">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="9310f-129">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="9310f-130">Разрешает успешное возвращение **CreateFolder** , возможно, перед тем, как новая папка будет полностью доступна вызывающему клиенту.</span><span class="sxs-lookup"><span data-stu-id="9310f-130">Allows **CreateFolder** to return successfully, possibly before the new folder is fully available to the calling client.</span></span> <span data-ttu-id="9310f-131">Если новая папка недоступна, то выполнение последующих вызовов может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="9310f-131">If the new folder is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="9310f-132">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9310f-132">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9310f-133">Имя папки имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="9310f-133">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="9310f-134">Если флаг МАПИ_УНИКОДЕ не установлен, имя папки указывается в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="9310f-134">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
<span data-ttu-id="9310f-135">ОПЕН_ИФ_ЕКСИСТС</span><span class="sxs-lookup"><span data-stu-id="9310f-135">OPEN_IF_EXISTS</span></span> 
  
> <span data-ttu-id="9310f-136">Позволяет успешно выполнить метод, даже если папка с именем, указанная в параметре _лпсзфолдернаме_ , уже существует, открыв существующую папку с таким именем.</span><span class="sxs-lookup"><span data-stu-id="9310f-136">Allows the method to succeed even if the folder named in the  _lpszFolderName_ parameter already exists by opening the existing folder that has that name.</span></span> <span data-ttu-id="9310f-137">Обратите внимание, что поставщики хранилищ сообщений, которые допускают наличие одинаковых папок на одном уровне, могут не открыть существующую папку, если существует более одной папки с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="9310f-137">Note that message store providers that allow sibling folders to have the same name might not open an existing folder if more than one exists with the supplied name.</span></span> 
    
 <span data-ttu-id="9310f-138">_Лппфолдер_</span><span class="sxs-lookup"><span data-stu-id="9310f-138">_lppFolder_</span></span>
  
> <span data-ttu-id="9310f-139">вышли Указатель на указатель на только что созданную папку.</span><span class="sxs-lookup"><span data-stu-id="9310f-139">[out] A pointer to a pointer to the newly created folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9310f-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9310f-140">Return value</span></span>

<span data-ttu-id="9310f-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="9310f-141">S_OK</span></span> 
  
> <span data-ttu-id="9310f-142">Новая папка успешно создана или открыта, если установлен флаг ОПЕН_ИФ_ЕКСИСТС.</span><span class="sxs-lookup"><span data-stu-id="9310f-142">The new folder has been successfully created or opened, if the OPEN_IF_EXISTS flag is set.</span></span>
    
<span data-ttu-id="9310f-143">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="9310f-143">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9310f-144">Установлен либо флаг МАПИ_УНИКОДЕ, либо реализация не поддерживает Юникод, или МАПИ_УНИКОДЕ не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="9310f-144">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="9310f-145">МАПИ_Е_КОЛЛИСИОН</span><span class="sxs-lookup"><span data-stu-id="9310f-145">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="9310f-146">Папка с именем, заданной в параметре _лпсзфолдернаме_ , уже существует.</span><span class="sxs-lookup"><span data-stu-id="9310f-146">A folder that has the name given in the  _lpszFolderName_ parameter already exists.</span></span> <span data-ttu-id="9310f-147">Имена папок должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="9310f-147">Folder names must be unique.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9310f-148">Примечания</span><span class="sxs-lookup"><span data-stu-id="9310f-148">Remarks</span></span>

<span data-ttu-id="9310f-149">Метод **IMAPIFolder:: CreateFolder** создает вложенную папку в текущей папке и присваивает новой папке идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="9310f-149">The **IMAPIFolder::CreateFolder** method creates a subfolder in the current folder and assigns an entry identifier to the new folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9310f-150">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9310f-150">Notes to callers</span></span>

<span data-ttu-id="9310f-151">При возвращении **CreateFolder** Обратите внимание, что идентификатор записи для новой папки может быть недоступен.</span><span class="sxs-lookup"><span data-stu-id="9310f-151">When **CreateFolder** returns, be aware that the entry identifier for the new folder might not be available.</span></span> <span data-ttu-id="9310f-152">Некоторые поставщики хранилищ сообщений не делают идентификаторы записей доступными до тех пор, пока не будет вызван метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) , чтобы сохранить его окончательно.</span><span class="sxs-lookup"><span data-stu-id="9310f-152">Some message store providers do not make entry identifiers available until after you have called the new folder's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to permanently save it.</span></span> <span data-ttu-id="9310f-153">Это особенно важно, если установлен флаг МАПИ_ДЕФЕРРЕД_ЕРРОРС.</span><span class="sxs-lookup"><span data-stu-id="9310f-153">This is especially true if you have set the MAPI_DEFERRED_ERRORS flag.</span></span> 
  
<span data-ttu-id="9310f-154">Обратите внимание, что некоторые поставщики хранилищ сообщений всегда назначают параметр _лппфолдер_ стандартному интерфейсу папки независимо от значения, передаваемого в качестве параметра _лпинтерфаце_ .</span><span class="sxs-lookup"><span data-stu-id="9310f-154">Be aware that some message store providers always point the  _lppFolder_ parameter to the folder's standard interface, regardless of the value that you pass in for the  _lpInterface_ parameter.</span></span> <span data-ttu-id="9310f-155">Так как возвращаемый указатель интерфейса может отличаться от ожидаемого типа, вызовите метод [IMAPIProp::](imapiprop-getprops.md) -PROPS новой папки, чтобы получить свойство **пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9310f-155">Because the interface pointer that is returned might not be of the type that you expect, call the new folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property.</span></span> <span data-ttu-id="9310f-156">При необходимости перед выполнением других вызовов приведите указатель к более подходящему типу.</span><span class="sxs-lookup"><span data-stu-id="9310f-156">If necessary, cast the pointer to a more appropriate type before you make other calls.</span></span>
  
<span data-ttu-id="9310f-157">Для большинства поставщиков хранилищ сообщений необходимо, чтобы имя новой папки было уникальным по отношению к именам ее родственных папок.</span><span class="sxs-lookup"><span data-stu-id="9310f-157">Most message store providers require the name of the new folder to be unique with respect to the names of its sibling folders.</span></span> <span data-ttu-id="9310f-158">Возможность обрабатывать значение ошибки МАПИ_Е_КОЛЛИСИОН, которое возвращается, если это правило не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9310f-158">Be able to handle the MAPI_E_COLLISION error value, which is returned if this rule is not followed.</span></span> 
  
<span data-ttu-id="9310f-159">Чтобы определить идентификатор записи только что созданной папки, вызовите метод **IMAPIProp::** -PROPS новой папки, чтобы получить свойство **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9310f-159">To determine the entry identifier of the newly created folder, call the new folder's **IMAPIProp::GetProps** method to retrieve its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9310f-160">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9310f-160">MFCMAPI reference</span></span>

<span data-ttu-id="9310f-161">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9310f-161">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9310f-162">**Файл**</span><span class="sxs-lookup"><span data-stu-id="9310f-162">**File**</span></span>|<span data-ttu-id="9310f-163">**Функция**</span><span class="sxs-lookup"><span data-stu-id="9310f-163">**Function**</span></span>|<span data-ttu-id="9310f-164">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9310f-164">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9310f-165">Мсгсторедлг. cpp</span><span class="sxs-lookup"><span data-stu-id="9310f-165">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="9310f-166">Кмсгсторедлг:: Онкреатесубфолдер</span><span class="sxs-lookup"><span data-stu-id="9310f-166">CMsgStoreDlg::OnCreateSubFolder</span></span>  <br/> |<span data-ttu-id="9310f-167">MFCMAPI использует метод **кмсгсторедлг:: онкреатесубфолдер** для создания новых папок в MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="9310f-167">MFCMAPI uses the **CMsgStoreDlg::OnCreateSubFolder** method to create new folders in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9310f-168">См. также</span><span class="sxs-lookup"><span data-stu-id="9310f-168">See also</span></span>



[<span data-ttu-id="9310f-169">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="9310f-169">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="9310f-170">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="9310f-170">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="9310f-171">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="9310f-171">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

