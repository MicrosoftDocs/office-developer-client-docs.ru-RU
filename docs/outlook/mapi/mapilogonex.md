---
title: MAPILogonEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPILogonEx
api_type:
- HeaderDef
ms.assetid: 98091e5b-1abd-4814-9c7a-583b420ee11d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9f2ec8f0ec00f7314982e9b112415f69901c358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424121"
---
# <a name="mapilogonex"></a><span data-ttu-id="9e327-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="9e327-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="9e327-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e327-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e327-105">Регистрирует клиентское приложение в сеансе с системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="9e327-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e327-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9e327-106">Header file:</span></span>  <br/> |<span data-ttu-id="9e327-107">Мапикс. h</span><span class="sxs-lookup"><span data-stu-id="9e327-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="9e327-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9e327-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9e327-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9e327-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9e327-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9e327-110">Called by:</span></span>  <br/> |<span data-ttu-id="9e327-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="9e327-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="9e327-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e327-112">Parameters</span></span>

 <span data-ttu-id="9e327-113">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="9e327-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="9e327-114">возврата Дескриптор окна, в котором диалоговое окно входа является модальным.</span><span class="sxs-lookup"><span data-stu-id="9e327-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="9e327-115">Если во время вызова не отображается диалоговое окно, параметр _улуипарам_ игнорируется.</span><span class="sxs-lookup"><span data-stu-id="9e327-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="9e327-116">Этот параметр может принимать нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="9e327-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="9e327-117">_лпсзпрофиленаме_</span><span class="sxs-lookup"><span data-stu-id="9e327-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="9e327-118">возврата Указатель на строку, содержащую имя профиля, который будет использоваться при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="9e327-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="9e327-119">Эта строка ограничена 64 символами.</span><span class="sxs-lookup"><span data-stu-id="9e327-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="9e327-120">_лпсзпассворд_</span><span class="sxs-lookup"><span data-stu-id="9e327-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="9e327-121">возврата Указатель на строку, содержащую пароль профиля.</span><span class="sxs-lookup"><span data-stu-id="9e327-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="9e327-122">Параметр _лпсзпассворд_ должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="9e327-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="9e327-123">_флфлагс_</span><span class="sxs-lookup"><span data-stu-id="9e327-123">_flFlags_</span></span>
  
> <span data-ttu-id="9e327-124">возврата Битовая маска флагов, используемых для управления выполнением входа.</span><span class="sxs-lookup"><span data-stu-id="9e327-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="9e327-125">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="9e327-125">The following flags can be set:</span></span>
    
<span data-ttu-id="9e327-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="9e327-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="9e327-127">Должен возвращаться общий сеанс, который позволяет клиентам позже получать сеанс без предоставления учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="9e327-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="9e327-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="9e327-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="9e327-129">Выполните вход в сеанс и выполните все операции в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="9e327-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="9e327-130">Как правило, если клиент планирует выполнить обработку в фоновом потоке или в отдельном процессе, который не может быть недоступен к основному потоку, он должен вызываться с флагом MAPI_BG_SESSION.</span><span class="sxs-lookup"><span data-stu-id="9e327-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="9e327-131">Клиентское приложение, такое как модуль индексирования или открытие файла личных папок (PST) для доступа к фоновому типу, — некоторые примеры того, где можно использовать MAPI_BG_SESSION. Мапилогонекс.</span><span class="sxs-lookup"><span data-stu-id="9e327-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="9e327-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="9e327-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="9e327-133">Профиль по умолчанию не должен использоваться, и пользователю необходимо предоставить профиль.</span><span class="sxs-lookup"><span data-stu-id="9e327-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="9e327-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="9e327-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="9e327-135">Войдите в систему с расширенными возможностями.</span><span class="sxs-lookup"><span data-stu-id="9e327-135">Log on with extended capabilities.</span></span> <span data-ttu-id="9e327-136">Этот флаг должен быть всегда установлен.</span><span class="sxs-lookup"><span data-stu-id="9e327-136">This flag should always be set.</span></span>
    
<span data-ttu-id="9e327-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="9e327-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="9e327-138">Перед возвратом необходимо выполнить попытку скачивания всех сообщений пользователя.</span><span class="sxs-lookup"><span data-stu-id="9e327-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="9e327-139">Если флаг MAPI_FORCE_DOWNLOAD не установлен, сообщения можно загружать в фоновом режиме после вызова метода Мапилогонекс.</span><span class="sxs-lookup"><span data-stu-id="9e327-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="9e327-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="9e327-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="9e327-141">Откроется диалоговое окно с запросом на ввод учетных данных при необходимости.</span><span class="sxs-lookup"><span data-stu-id="9e327-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="9e327-142">Если флаг MAPI_LOGON_UI не установлен, вызывающий клиент не отображает диалоговое окно входа и возвращает значение ошибки, если пользователь не вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="9e327-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="9e327-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="9e327-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="9e327-144">Необходимо выполнить попытку создания нового сеанса MAPI вместо получения общего сеанса.</span><span class="sxs-lookup"><span data-stu-id="9e327-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="9e327-145">Если флаг MAPI_NEW_SESSION не задан, Мапилогонекс использует существующий общий сеанс, даже если параметр _лпсзпрофиленаме_ имеет значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="9e327-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="9e327-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="9e327-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="9e327-147">MAPI не должен сообщать диспетчеру MAPI о существовании сеанса.</span><span class="sxs-lookup"><span data-stu-id="9e327-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="9e327-148">Результат заключается в том, что сообщения не могут быть отправлены или получены в сеансе, за исключением с помощью тесно связанных хранилища и пары транспорта.</span><span class="sxs-lookup"><span data-stu-id="9e327-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="9e327-149">Вызывающий клиент устанавливает этот флаг, если он действует как агент, если необходимо выполнить действия по настройке, или если клиент выполняет просмотр доступных хранилищ сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e327-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="9e327-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="9e327-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="9e327-151">Вызывающий абонент работает как служба Windows.</span><span class="sxs-lookup"><span data-stu-id="9e327-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="9e327-152">Вызывающие абоненты, которые не работают как служба Windows, не должны устанавливать этот флаг; для абонентов, работающих в качестве службы, необходимо установить этот флаг.</span><span class="sxs-lookup"><span data-stu-id="9e327-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="9e327-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="9e327-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="9e327-154">Мапилогонекс должно отображать диалоговое окно конфигурации для каждой службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="9e327-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="9e327-155">Диалоговые окна отображаются после выбора профиля, но перед входом в систему любой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e327-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="9e327-156">В общем диалоговом окне MAPI для входа также имеется флажок, который запрашивает одну и ту же операцию.</span><span class="sxs-lookup"><span data-stu-id="9e327-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="9e327-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="9e327-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="9e327-158">При блокировании в течение нескольких секунд произойдет ошибка входа в систему.</span><span class="sxs-lookup"><span data-stu-id="9e327-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="9e327-159">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9e327-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9e327-160">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="9e327-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="9e327-161">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="9e327-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="9e327-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="9e327-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="9e327-163">Подсистема обмена сообщениями должна заменить имя профиля профиля по умолчанию для параметра _лпсзпрофиленаме_ .</span><span class="sxs-lookup"><span data-stu-id="9e327-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="9e327-164">Флаг MAPI_EXPLICIT_PROFILE игнорируется, если _лпсзпрофиленаме_ не имеет значение null или не задано значение null.</span><span class="sxs-lookup"><span data-stu-id="9e327-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="9e327-165">_лппсессион_</span><span class="sxs-lookup"><span data-stu-id="9e327-165">_lppSession_</span></span>
  
> <span data-ttu-id="9e327-166">вышли Указатель на указатель на интерфейс сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e327-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9e327-167">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e327-167">Return value</span></span>

<span data-ttu-id="9e327-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e327-168">S_OK</span></span> 
  
> <span data-ttu-id="9e327-169">Вход выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="9e327-169">The logon succeeded.</span></span>
    
<span data-ttu-id="9e327-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="9e327-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="9e327-171">Не удалось выполнить вход в систему из-за того, что один или несколько параметров Мапилогонекс недопустимы или в связи с тем, что уже открыто слишком много сеансов.</span><span class="sxs-lookup"><span data-stu-id="9e327-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="9e327-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="9e327-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="9e327-173">MAPI сериализует все входы в систему с помощью мьютекса.</span><span class="sxs-lookup"><span data-stu-id="9e327-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="9e327-174">Возвращается, если установлен флаг MAPI_TIMEOUT_SHORT и другой поток удерживал мьютекс.</span><span class="sxs-lookup"><span data-stu-id="9e327-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="9e327-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="9e327-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="9e327-176">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="9e327-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9e327-177">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e327-177">Remarks</span></span>

<span data-ttu-id="9e327-178">Клиентские приложения MAPI вызывают функцию Мапилогонекс для входа в сеанс с системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="9e327-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="9e327-179">Все строки, которые передаются и возвращаются из вызовов MAPI, завершаются нулем и должны быть указаны в текущем наборе символов или на странице кодов в операционной системе клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="9e327-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="9e327-180">Параметр _лпсзпрофиленаме_ игнорируется, если существует предыдущий сеанс, вызвавший мапилогонекс с установленным флагом MAPI_ALLOW_OTHERS и если флаг MAPI_NEW_SESSION не задан.</span><span class="sxs-lookup"><span data-stu-id="9e327-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="9e327-181">Если параметр _лпсзпрофиленаме_ имеет значение null или указывает на пустую строку, а параметр _флфлагс_ содержит флаг MAPI_LOGON_UI, функция мапилогонекс создает диалоговое окно входа с пустым полем для имени профиля.</span><span class="sxs-lookup"><span data-stu-id="9e327-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="9e327-182">При входе в определенный профиль клиент должен передать MAPI_NEW_SESSIONный флаг в Мапилогонекс в дополнение к имени профиля.</span><span class="sxs-lookup"><span data-stu-id="9e327-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="9e327-183">В противном случае, если другой клиент установил общий сеанс, войдя в систему MAPI_ALLOW_OTHERS, то клиент будет входить в общий сеанс, а не в запрошенный профиль.</span><span class="sxs-lookup"><span data-stu-id="9e327-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="9e327-184">Флаг MAPI_EXPLICIT_PROFILE не приводит к использованию имени профиля по умолчанию, если _лпсзпрофиленаме_ имеет значение null, или пустое значение, если также не указан флаг MAPI_USE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="9e327-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="9e327-185">Флаг MAPI_NO_MAIL имеет несколько эффектов, которые приводят к возникновению следующего, если не используется диспетчер очереди MAPI:</span><span class="sxs-lookup"><span data-stu-id="9e327-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="9e327-186">В течение этого сеанса Диспетчер очереди MAPI не может отправлять или доставлять сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e327-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="9e327-187">Только тесно связанные поставщики услуг хранения и транспорта могут отправлять и доставлять сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e327-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="9e327-188">Хранилища на сервере могут по-прежнему отправлять и доставлять сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e327-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="9e327-189">Сообщения, отправленные или доставляемые хранилищами на сервере, не обрабатываются какими-либо поставщиками обработчиков.</span><span class="sxs-lookup"><span data-stu-id="9e327-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="9e327-190">Параметры для отдельных сообщений и получателей для транспортов недоступны.</span><span class="sxs-lookup"><span data-stu-id="9e327-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="9e327-191">Таблица Status не содержит записей для поставщиков транспорта, а все функции транспорта, зависящие от объектов Status (например, Configuration), недоступны.</span><span class="sxs-lookup"><span data-stu-id="9e327-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="9e327-192">Строка "Диспетчер очереди сообщений" в таблице "состояние" содержит значение STATUS_FAILURE.</span><span class="sxs-lookup"><span data-stu-id="9e327-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="9e327-193">Вход в пиггибаккед разрешен, но эти входы не приводят к предыдущему входу в систему для получения обновлений объекта Status.</span><span class="sxs-lookup"><span data-stu-id="9e327-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="9e327-194">Служба всегда должна входить в систему с помощью флага MAPI_NO_MAIL.</span><span class="sxs-lookup"><span data-stu-id="9e327-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9e327-195">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9e327-195">MFCMAPI reference</span></span>

<span data-ttu-id="9e327-196">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9e327-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9e327-197">**Файл**</span><span class="sxs-lookup"><span data-stu-id="9e327-197">**File**</span></span>|<span data-ttu-id="9e327-198">**Функция**</span><span class="sxs-lookup"><span data-stu-id="9e327-198">**Function**</span></span>|<span data-ttu-id="9e327-199">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9e327-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9e327-200">Мапиобжектс. cpp</span><span class="sxs-lookup"><span data-stu-id="9e327-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="9e327-201">Кмапиобжектс:: Мапилогонекс</span><span class="sxs-lookup"><span data-stu-id="9e327-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="9e327-202">MFCMAPI использует метод Мапилогонекс для входа в MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e327-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e327-203">См. также</span><span class="sxs-lookup"><span data-stu-id="9e327-203">See also</span></span>



[<span data-ttu-id="9e327-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="9e327-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="9e327-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="9e327-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="9e327-206">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="9e327-206">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

