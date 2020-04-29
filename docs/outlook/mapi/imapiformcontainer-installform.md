---
title: имапиформконтаинеринсталлформ
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
# <a name="imapiformcontainerinstallform"></a><span data-ttu-id="5dec6-103">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="5dec6-103">IMAPIFormContainer::InstallForm</span></span>

  
  
<span data-ttu-id="5dec6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5dec6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5dec6-105">Устанавливает форму в библиотеку форм.</span><span class="sxs-lookup"><span data-stu-id="5dec6-105">Installs a form into a form library.</span></span>
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a><span data-ttu-id="5dec6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5dec6-106">Parameters</span></span>

 <span data-ttu-id="5dec6-107">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="5dec6-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="5dec6-108">возврата Дескриптор родительского окна всех диалоговых окон и окон, отображаемых данным методом.</span><span class="sxs-lookup"><span data-stu-id="5dec6-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="5dec6-109">Параметр _улуипарам_ игнорируется, если клиентское приложение не устанавливает флаг MAPI_DIALOG в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="5dec6-109">The  _ulUIParam_ parameter is ignored unless the client application sets the MAPI_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="5dec6-110">Параметр _улуипарам_ может иметь значение null, если MAPI_DIALOG еще не передан.</span><span class="sxs-lookup"><span data-stu-id="5dec6-110">The  _ulUIParam_ parameter can be NULL if MAPI_DIALOG is not also passed.</span></span> 
    
 <span data-ttu-id="5dec6-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5dec6-111">_ulFlags_</span></span>
  
> <span data-ttu-id="5dec6-112">возврата Битовая маска флагов, управляющих установкой формы.</span><span class="sxs-lookup"><span data-stu-id="5dec6-112">[in] A bitmask of flags that controls the installation of the form.</span></span> <span data-ttu-id="5dec6-113">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="5dec6-113">The following flags can be set:</span></span>
    
<span data-ttu-id="5dec6-114">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="5dec6-114">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="5dec6-115">Отображает диалоговое окно для получения сведений о ходе выполнения или приглашения пользователя на дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="5dec6-115">Displays a dialog box to provide progress information or prompt the user for more information.</span></span> <span data-ttu-id="5dec6-116">Если этот флаг не установлен, диалоговое окно не отображается.</span><span class="sxs-lookup"><span data-stu-id="5dec6-116">If this flag is not set, no dialog box is displayed.</span></span>
    
<span data-ttu-id="5dec6-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5dec6-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5dec6-118">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="5dec6-118">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="5dec6-119">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="5dec6-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="5dec6-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span><span class="sxs-lookup"><span data-stu-id="5dec6-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span></span> 
  
> <span data-ttu-id="5dec6-121">Если уже существует другая форма, которая обрабатывает класс сообщений, обрабатываемый этой формой, замените существующую форму на эту.</span><span class="sxs-lookup"><span data-stu-id="5dec6-121">If another form already exists that handles the message class handled by this form, replace the existing form with this one.</span></span> <span data-ttu-id="5dec6-122">Этот флаг игнорируется, если также присутствует флаг MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="5dec6-122">This flag is ignored if the MAPI_DIALOG flag is also present.</span></span> 
    
 <span data-ttu-id="5dec6-123">_сзкфгпаснаме_</span><span class="sxs-lookup"><span data-stu-id="5dec6-123">_szCfgPathName_</span></span>
  
> <span data-ttu-id="5dec6-124">возврата Путь к файлу конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="5dec6-124">[in] The path to the form's configuration file.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5dec6-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5dec6-125">Return value</span></span>

<span data-ttu-id="5dec6-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="5dec6-126">S_OK</span></span> 
  
> <span data-ttu-id="5dec6-127">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="5dec6-127">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="5dec6-128">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="5dec6-128">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="5dec6-129">Произошла ошибка реализации.</span><span class="sxs-lookup"><span data-stu-id="5dec6-129">An implementation error occurred.</span></span> <span data-ttu-id="5dec6-130">Чтобы получить структуру [мапиеррор](mapierror.md) , связанную с ошибкой, вызовите метод [Имапиформконтаинер:: GetLastError](imapiformcontainer-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5dec6-130">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="5dec6-131">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="5dec6-131">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="5dec6-132">Пользователь отменил установку формы, обычно нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="5dec6-132">The user canceled the installation of the form, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="5dec6-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="5dec6-133">Notes to implementers</span></span>

<span data-ttu-id="5dec6-134">Поставщики библиотеки форм должны заполнить структуру **мапиеррор** и возвращать MAPI_E_EXTENDED_ERROR при выполнении любого из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="5dec6-134">Form library providers should fill in a **MAPIERROR** structure and return MAPI_E_EXTENDED_ERROR if any of the following conditions occur:</span></span> 
  
- <span data-ttu-id="5dec6-135">Файл конфигурации не найден.</span><span class="sxs-lookup"><span data-stu-id="5dec6-135">The configuration file is not found.</span></span>
    
- <span data-ttu-id="5dec6-136">Файл конфигурации недоступен для чтения.</span><span class="sxs-lookup"><span data-stu-id="5dec6-136">The configuration file is not readable.</span></span>
    
- <span data-ttu-id="5dec6-137">Недопустимый файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5dec6-137">The configuration file is invalid.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="5dec6-138">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="5dec6-138">Notes to callers</span></span>

<span data-ttu-id="5dec6-139">Клиентские приложения вызывают метод **имапиформконтаинер:: инсталлформ** для установки формы в определенный контейнер форм.</span><span class="sxs-lookup"><span data-stu-id="5dec6-139">Client applications call the **IMAPIFormContainer::InstallForm** method to install a form into a specific form container.</span></span> <span data-ttu-id="5dec6-140">Параметр _сзкфгпаснаме_ должен содержать путь к файлу конфигурации формы (то есть, файл с расширением. cfg, который описывает форму и ее реализацию).</span><span class="sxs-lookup"><span data-stu-id="5dec6-140">The  _szCfgPathName_ parameter must contain the path of a form configuration file (that is, a file with the .cfg extension that describes the form and its implementation).</span></span> <span data-ttu-id="5dec6-141">Флаги в параметре _ulFlags_ определяют следующее:</span><span class="sxs-lookup"><span data-stu-id="5dec6-141">The flags in the  _ulFlags_ parameter specify the following:</span></span> 
  
- <span data-ttu-id="5dec6-142">Если установлен флаг MAPI_DIALOG, отображается пользовательский интерфейс, который позволяет пользователю, устанавливающему форму, указать сведения об установке.</span><span class="sxs-lookup"><span data-stu-id="5dec6-142">If the MAPI_DIALOG flag is set, a user interface is displayed, enabling the user who is installing the form to specify installation details.</span></span>
    
- <span data-ttu-id="5dec6-143">Если установлен флаг MAPIFORM_INSTALL_OVERWRITEONCONFLICT, все предыдущие формы для того же класса сообщений заменяются на устанавливаемую форму.</span><span class="sxs-lookup"><span data-stu-id="5dec6-143">If the MAPIFORM_INSTALL_OVERWRITEONCONFLICT flag is set, any previous form for the same message class is replaced with the form being installed.</span></span> <span data-ttu-id="5dec6-144">В противном случае установка формы объединяется с текущим описанием формы (если оно существует).</span><span class="sxs-lookup"><span data-stu-id="5dec6-144">Otherwise, the form installation is merged with the current form description, if one exists.</span></span>
    
- <span data-ttu-id="5dec6-145">Если задано значение MAPI_DIALOG, MAPIFORM_INSTALL_OVERWRITEONCONFLICT игнорируется.</span><span class="sxs-lookup"><span data-stu-id="5dec6-145">If MAPI_DIALOG is set, MAPIFORM_INSTALL_OVERWRITEONCONFLICT is ignored.</span></span>
    
- <span data-ttu-id="5dec6-146">Отсутствие MAPIFORM_INSTALL_OVERWRITEONCONFLICT в наборе флагов означает, что слияние будет выполнено.</span><span class="sxs-lookup"><span data-stu-id="5dec6-146">The absence of MAPIFORM_INSTALL_OVERWRITEONCONFLICT in the flag set means that a merge will be done.</span></span> <span data-ttu-id="5dec6-147">Все новые платформы в файле. cfg, которые в настоящее время не указаны в описании формы, будут установлены и никакие другие изменения не будут выполнены.</span><span class="sxs-lookup"><span data-stu-id="5dec6-147">Any new platforms in the .cfg file that are not currently present in the form description will be installed and no other changes will occur.</span></span>
    
- <span data-ttu-id="5dec6-148">Если установлен флаг MAPI_UNICODE, путь к файлу конфигурации формы представляет собой строку в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="5dec6-148">If the MAPI_UNICODE flag is set, the path of the form configuration file is a Unicode string.</span></span> 
    
<span data-ttu-id="5dec6-149">Клиенты должны вызывать [имапиформконтаинер:: GetLastError](imapiformcontainer-getlasterror.md) , если **инсталлформ** возвращает MAPI_E_EXTENDED_ERROR, и должны проверить возвращаемую структуру [мапиеррор](mapierror.md) , чтобы определить условие, вызвавшее ошибку.</span><span class="sxs-lookup"><span data-stu-id="5dec6-149">Clients should call [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) if **InstallForm** returns MAPI_E_EXTENDED_ERROR, and they should check the returned [MAPIERROR](mapierror.md) structure to determine the condition that raised the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5dec6-150">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5dec6-150">MFCMAPI reference</span></span>

<span data-ttu-id="5dec6-151">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="5dec6-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5dec6-152">**Файл**</span><span class="sxs-lookup"><span data-stu-id="5dec6-152">**File**</span></span>|<span data-ttu-id="5dec6-153">**Функция**</span><span class="sxs-lookup"><span data-stu-id="5dec6-153">**Function**</span></span>|<span data-ttu-id="5dec6-154">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="5dec6-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5dec6-155">Формконтаинердлг. cpp</span><span class="sxs-lookup"><span data-stu-id="5dec6-155">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="5dec6-156">Кформконтаинердлг:: Онинсталлформ</span><span class="sxs-lookup"><span data-stu-id="5dec6-156">CFormContainerDlg::OnInstallForm</span></span>  <br/> |<span data-ttu-id="5dec6-157">MFCMAPI использует метод **имапиформконтаинер:: инсталлформ** для установки формы в контейнере форм.</span><span class="sxs-lookup"><span data-stu-id="5dec6-157">MFCMAPI uses the **IMAPIFormContainer::InstallForm** method to install a form in a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5dec6-158">См. также</span><span class="sxs-lookup"><span data-stu-id="5dec6-158">See also</span></span>



[<span data-ttu-id="5dec6-159">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="5dec6-159">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="5dec6-160">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5dec6-160">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="5dec6-161">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="5dec6-161">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

