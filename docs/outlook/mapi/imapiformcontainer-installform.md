---
title: Имапиформконтаинеринсталлформ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.InstallForm
api_type:
- COM
ms.assetid: b39ca52c-4dbe-41c0-9e1b-3998a9dc9742
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a0650033e4fea79046eac5757e3d0deb963c38e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405088"
---
# <a name="imapiformcontainerinstallform"></a><span data-ttu-id="bc89d-103">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="bc89d-103">IMAPIFormContainer::InstallForm</span></span>

  
  
<span data-ttu-id="bc89d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc89d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc89d-105">Устанавливает форму в библиотеку форм.</span><span class="sxs-lookup"><span data-stu-id="bc89d-105">Installs a form into a form library.</span></span>
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a><span data-ttu-id="bc89d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc89d-106">Parameters</span></span>

 <span data-ttu-id="bc89d-107">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="bc89d-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="bc89d-108">возврата Дескриптор родительского окна всех диалоговых окон и окон, отображаемых данным методом.</span><span class="sxs-lookup"><span data-stu-id="bc89d-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="bc89d-109">Параметр _улуипарам_ игнорируется, если клиентское приложение не устанавливает флаг мапи_диалог в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="bc89d-109">The  _ulUIParam_ parameter is ignored unless the client application sets the MAPI_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="bc89d-110">Параметр _улуипарам_ может иметь значение null, если мапи_диалог также не передан.</span><span class="sxs-lookup"><span data-stu-id="bc89d-110">The  _ulUIParam_ parameter can be NULL if MAPI_DIALOG is not also passed.</span></span> 
    
 <span data-ttu-id="bc89d-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bc89d-111">_ulFlags_</span></span>
  
> <span data-ttu-id="bc89d-112">возврата Битовая маска флагов, управляющих установкой формы.</span><span class="sxs-lookup"><span data-stu-id="bc89d-112">[in] A bitmask of flags that controls the installation of the form.</span></span> <span data-ttu-id="bc89d-113">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="bc89d-113">The following flags can be set:</span></span>
    
<span data-ttu-id="bc89d-114">МАПИ_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="bc89d-114">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="bc89d-115">Отображает диалоговое окно для получения сведений о ходе выполнения или приглашения пользователя на дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="bc89d-115">Displays a dialog box to provide progress information or prompt the user for more information.</span></span> <span data-ttu-id="bc89d-116">Если этот флаг не установлен, диалоговое окно не отображается.</span><span class="sxs-lookup"><span data-stu-id="bc89d-116">If this flag is not set, no dialog box is displayed.</span></span>
    
<span data-ttu-id="bc89d-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bc89d-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bc89d-118">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="bc89d-118">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="bc89d-119">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="bc89d-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="bc89d-120">МАПИФОРМ_ИНСТАЛЛ_ОВЕРВРИТЕОНКОНФЛИКТ</span><span class="sxs-lookup"><span data-stu-id="bc89d-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span></span> 
  
> <span data-ttu-id="bc89d-121">Если уже существует другая форма, которая обрабатывает класс сообщений, обрабатываемый этой формой, замените существующую форму на эту.</span><span class="sxs-lookup"><span data-stu-id="bc89d-121">If another form already exists that handles the message class handled by this form, replace the existing form with this one.</span></span> <span data-ttu-id="bc89d-122">Этот флаг игнорируется, если также присутствует флаг МАПИ_ДИАЛОГ.</span><span class="sxs-lookup"><span data-stu-id="bc89d-122">This flag is ignored if the MAPI_DIALOG flag is also present.</span></span> 
    
 <span data-ttu-id="bc89d-123">_Сзкфгпаснаме_</span><span class="sxs-lookup"><span data-stu-id="bc89d-123">_szCfgPathName_</span></span>
  
> <span data-ttu-id="bc89d-124">возврата Путь к файлу конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="bc89d-124">[in] The path to the form's configuration file.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bc89d-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc89d-125">Return value</span></span>

<span data-ttu-id="bc89d-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="bc89d-126">S_OK</span></span> 
  
> <span data-ttu-id="bc89d-127">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="bc89d-127">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="bc89d-128">МАПИ_Е_ЕКСТЕНДЕД_ЕРРОР</span><span class="sxs-lookup"><span data-stu-id="bc89d-128">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="bc89d-129">Произошла ошибка реализации.</span><span class="sxs-lookup"><span data-stu-id="bc89d-129">An implementation error occurred.</span></span> <span data-ttu-id="bc89d-130">Чтобы получить структуру [мапиеррор](mapierror.md) , связанную с ошибкой, вызовите метод [Имапиформконтаинер:: GetLastError](imapiformcontainer-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="bc89d-130">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="bc89d-131">МАПИ_Е_УСЕР_КАНЦЕЛ</span><span class="sxs-lookup"><span data-stu-id="bc89d-131">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="bc89d-132">Пользователь отменил установку формы, обычно нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="bc89d-132">The user canceled the installation of the form, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="bc89d-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="bc89d-133">Notes to implementers</span></span>

<span data-ttu-id="bc89d-134">Поставщики библиотеки форм должны заполнить структуру **мапиеррор** и вернуть мапи_е_екстендед_еррор, если выполняются какие – либо из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="bc89d-134">Form library providers should fill in a **MAPIERROR** structure and return MAPI_E_EXTENDED_ERROR if any of the following conditions occur:</span></span> 
  
- <span data-ttu-id="bc89d-135">Файл конфигурации не найден.</span><span class="sxs-lookup"><span data-stu-id="bc89d-135">The configuration file is not found.</span></span>
    
- <span data-ttu-id="bc89d-136">Файл конфигурации недоступен для чтения.</span><span class="sxs-lookup"><span data-stu-id="bc89d-136">The configuration file is not readable.</span></span>
    
- <span data-ttu-id="bc89d-137">Недопустимый файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bc89d-137">The configuration file is invalid.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="bc89d-138">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="bc89d-138">Notes to callers</span></span>

<span data-ttu-id="bc89d-139">Клиентские приложения вызывают метод **имапиформконтаинер:: инсталлформ** для установки формы в определенный контейнер форм.</span><span class="sxs-lookup"><span data-stu-id="bc89d-139">Client applications call the **IMAPIFormContainer::InstallForm** method to install a form into a specific form container.</span></span> <span data-ttu-id="bc89d-140">Параметр _сзкфгпаснаме_ должен содержать путь к файлу конфигурации формы (то есть, файл с расширением. cfg, который описывает форму и ее реализацию).</span><span class="sxs-lookup"><span data-stu-id="bc89d-140">The  _szCfgPathName_ parameter must contain the path of a form configuration file (that is, a file with the .cfg extension that describes the form and its implementation).</span></span> <span data-ttu-id="bc89d-141">Флаги в параметре _ulFlags_ определяют следующее:</span><span class="sxs-lookup"><span data-stu-id="bc89d-141">The flags in the  _ulFlags_ parameter specify the following:</span></span> 
  
- <span data-ttu-id="bc89d-142">Если установлен флаг МАПИ_ДИАЛОГ, отображается пользовательский интерфейс, который позволяет пользователю, устанавливающему форму, указать сведения об установке.</span><span class="sxs-lookup"><span data-stu-id="bc89d-142">If the MAPI_DIALOG flag is set, a user interface is displayed, enabling the user who is installing the form to specify installation details.</span></span>
    
- <span data-ttu-id="bc89d-143">Если установлен флаг МАПИФОРМ_ИНСТАЛЛ_ОВЕРВРИТЕОНКОНФЛИКТ, все предыдущие формы для того же класса сообщений заменяются на устанавливаемую форму.</span><span class="sxs-lookup"><span data-stu-id="bc89d-143">If the MAPIFORM_INSTALL_OVERWRITEONCONFLICT flag is set, any previous form for the same message class is replaced with the form being installed.</span></span> <span data-ttu-id="bc89d-144">В противном случае установка формы объединяется с текущим описанием формы (если оно существует).</span><span class="sxs-lookup"><span data-stu-id="bc89d-144">Otherwise, the form installation is merged with the current form description, if one exists.</span></span>
    
- <span data-ttu-id="bc89d-145">Если задано значение МАПИ_ДИАЛОГ, МАПИФОРМ_ИНСТАЛЛ_ОВЕРВРИТЕОНКОНФЛИКТ игнорируется.</span><span class="sxs-lookup"><span data-stu-id="bc89d-145">If MAPI_DIALOG is set, MAPIFORM_INSTALL_OVERWRITEONCONFLICT is ignored.</span></span>
    
- <span data-ttu-id="bc89d-146">Отсутствие МАПИФОРМ_ИНСТАЛЛ_ОВЕРВРИТЕОНКОНФЛИКТ в установленном флаге означает, что слияние будет выполнено.</span><span class="sxs-lookup"><span data-stu-id="bc89d-146">The absence of MAPIFORM_INSTALL_OVERWRITEONCONFLICT in the flag set means that a merge will be done.</span></span> <span data-ttu-id="bc89d-147">Все новые платформы в файле. cfg, которые в настоящее время не указаны в описании формы, будут установлены и никакие другие изменения не будут выполнены.</span><span class="sxs-lookup"><span data-stu-id="bc89d-147">Any new platforms in the .cfg file that are not currently present in the form description will be installed and no other changes will occur.</span></span>
    
- <span data-ttu-id="bc89d-148">Если установлен флаг МАПИ_УНИКОДЕ, путь к файлу конфигурации формы представляет собой строку в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="bc89d-148">If the MAPI_UNICODE flag is set, the path of the form configuration file is a Unicode string.</span></span> 
    
<span data-ttu-id="bc89d-149">Клиенты должны вызывать [имапиформконтаинер:: GetLastError](imapiformcontainer-getlasterror.md) , если **инсталлформ** возвращает мапи_е_екстендед_еррор, и должны проверить возвращаемую структуру [мапиеррор](mapierror.md) , чтобы определить условие, вызвавшее ошибку.</span><span class="sxs-lookup"><span data-stu-id="bc89d-149">Clients should call [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) if **InstallForm** returns MAPI_E_EXTENDED_ERROR, and they should check the returned [MAPIERROR](mapierror.md) structure to determine the condition that raised the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bc89d-150">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bc89d-150">MFCMAPI reference</span></span>

<span data-ttu-id="bc89d-151">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="bc89d-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bc89d-152">**Файл**</span><span class="sxs-lookup"><span data-stu-id="bc89d-152">**File**</span></span>|<span data-ttu-id="bc89d-153">**Функция**</span><span class="sxs-lookup"><span data-stu-id="bc89d-153">**Function**</span></span>|<span data-ttu-id="bc89d-154">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="bc89d-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bc89d-155">Формконтаинердлг. cpp</span><span class="sxs-lookup"><span data-stu-id="bc89d-155">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="bc89d-156">Кформконтаинердлг:: Онинсталлформ</span><span class="sxs-lookup"><span data-stu-id="bc89d-156">CFormContainerDlg::OnInstallForm</span></span>  <br/> |<span data-ttu-id="bc89d-157">MFCMAPI использует метод **имапиформконтаинер:: инсталлформ** для установки формы в контейнере форм.</span><span class="sxs-lookup"><span data-stu-id="bc89d-157">MFCMAPI uses the **IMAPIFormContainer::InstallForm** method to install a form in a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bc89d-158">См. также</span><span class="sxs-lookup"><span data-stu-id="bc89d-158">See also</span></span>



[<span data-ttu-id="bc89d-159">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="bc89d-159">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="bc89d-160">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bc89d-160">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="bc89d-161">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="bc89d-161">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

