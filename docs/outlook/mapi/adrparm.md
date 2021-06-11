---
title: ADRPARM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRPARM
api_type:
- COM
ms.assetid: 35cd57b4-9901-456c-bf06-1f84e274eb4e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9663a25a50d914f47cff48124898d16318bbbc43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425899"
---
# <a name="adrparm"></a><span data-ttu-id="5f4a4-103">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="5f4a4-103">ADRPARM</span></span>

<span data-ttu-id="5f4a4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f4a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f4a4-105">Описывает отображение и поведение диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-105">Describes the display and behavior of the common address dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5f4a4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5f4a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="5f4a4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f4a4-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ADRPARM
{
  ULONG cbABContEntryID;
  LPENTRYID lpABContEntryID;
  ULONG ulFlags;
  LPVOID lpReserved;
  ULONG ulHelpContext;
  LPSTR lpszHelpFileName;
  LPFNABSDI lpfnABSDI;
  LPFNDISMISS lpfnDismiss;
  LPVOID lpvDismissContext;
  LPSTR lpszCaption;
  LPSTR lpszNewEntryTitle;
  LPSTR lpszDestWellsTitle;
  ULONG cDestFields;
  ULONG nDestFieldFocus;
  LPSTR FAR *lppszDestTitles;
  ULONG FAR *lpulDestComps;
  LPSRestriction lpContRestriction;
  LPSRestriction lpHierRestriction;
} ADRPARM, FAR *LPADRPARM;

```

## <a name="members"></a><span data-ttu-id="5f4a4-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="5f4a4-108">Members</span></span>

<span data-ttu-id="5f4a4-109">**cbABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-109">**cbABContEntryID**</span></span>
  
> <span data-ttu-id="5f4a4-110">Количество bytes в идентификаторе записи, на который указывает **lpABContEntryID.**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-110">Count of bytes in the entry identifier pointed to by **lpABContEntryID**.</span></span>
    
<span data-ttu-id="5f4a4-111">**lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-111">**lpABContEntryID**</span></span>
  
> <span data-ttu-id="5f4a4-112">Указатель на идентификатор входа контейнера, который поставляет начальный список адресов получателей, отображаемого в диалоговом окне адресов.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-112">Pointer to the entry identifier of the container that supplies the initial list of recipient addresses that are displayed in the address dialog box.</span></span>
    
<span data-ttu-id="5f4a4-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-113">**ulFlags**</span></span>
  
> <span data-ttu-id="5f4a4-114">Bitmask флагов, связанных с различными вариантами диалоговых адресов.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-114">Bitmask of flags associated with various address dialog box options.</span></span> <span data-ttu-id="5f4a4-115">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="5f4a4-115">The following flags can be set:</span></span>
    
<span data-ttu-id="5f4a4-116">AB_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="5f4a4-116">AB_RESOLVE</span></span>
  
> <span data-ttu-id="5f4a4-117">Разрешить все имена после закрытия диалогового окна с адресом.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-117">Enable all names to be resolved after the address dialog box is closed.</span></span> <span data-ttu-id="5f4a4-118">Если есть неоднозначные записи, которые являются результатом процесса разрешения имен, диалоговое окно, как представляется, вызывает у пользователя помощь в их разрешении.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-118">If there are ambiguous entries that result from the name resolution process, a dialog box appears to prompt the user for help in resolving them.</span></span> <span data-ttu-id="5f4a4-119">Установка этого флага гарантирует, что все имена, возвращенные [IAddrBook::Address,](iaddrbook-address.md) будут разрешены.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-119">Setting this flag guarantees that all of the names returned by [IAddrBook::Address](iaddrbook-address.md) are resolved.</span></span> 
    
<span data-ttu-id="5f4a4-120">AB_SELECTONLY</span><span class="sxs-lookup"><span data-stu-id="5f4a4-120">AB_SELECTONLY</span></span>
  
> <span data-ttu-id="5f4a4-121">Отключить создание разных адресов для списка получателей.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-121">Disable the creation of one-off addresses for a recipient list.</span></span> <span data-ttu-id="5f4a4-122">Этот флаг используется только в том случае, если диалоговое окно является модальным, как указывается DIALOG_MODAL заданной флагом.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-122">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span>
    
<span data-ttu-id="5f4a4-123">ADDRESS_ONE</span><span class="sxs-lookup"><span data-stu-id="5f4a4-123">ADDRESS_ONE</span></span>
  
> <span data-ttu-id="5f4a4-124">Пользователь может выбрать именно одного получателя, а не нескольких получателей из списка.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-124">The user can select exactly one recipient instead of multiple recipients from a list.</span></span> <span data-ttu-id="5f4a4-125">Этот флаг действителен только в том случае, если **значение cDestFields** нулевое и диалоговое окно является модальным, как указывается в DIALOG_MODAL заданной отметке.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-125">This flag is valid only when **cDestFields** is zero and the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="5f4a4-126">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="5f4a4-126">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="5f4a4-127">Вызывает отображение модальной версии диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-127">Causes the modal version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="5f4a4-128">Этот флаг или DIALOG_SDI должен быть заданной; они не могут быть установлены.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-128">Either this flag or DIALOG_SDI should be set; they cannot both be set.</span></span> 
    
<span data-ttu-id="5f4a4-129">DIALOG_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="5f4a4-129">DIALOG_OPTIONS</span></span>
  
> <span data-ttu-id="5f4a4-130">Вызывает отображение кнопки **"Параметры** отправки" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-130">Causes the **Send Options** button to be displayed in the dialog box.</span></span> <span data-ttu-id="5f4a4-131">Этот флаг используется только в том случае, если диалоговое окно является модальным, как указывается DIALOG_MODAL заданной флагом.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-131">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="5f4a4-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="5f4a4-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="5f4a4-133">Вызывает отображённую версию общего диалогового окна адресов.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-133">Causes the modeless version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="5f4a4-134">Этот флаг или DIALOG_MODAL должен быть заданной; они не могут быть установлены.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-134">Either this flag or DIALOG_MODAL should be set; they cannot both be set.</span></span> <span data-ttu-id="5f4a4-135">Флаг DIALOG_SDI игнорируется для клиентов, не Outlook, и будет отображаться модальная версия диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-135">The DIALOG_SDI flag is ignored for non-Outlook clients, and the modal version of the dialog box will be displayed.</span></span> <span data-ttu-id="5f4a4-136">Следовательно, указатель на ручку не следует ожидать в параметре _lpulUIParam_ [IAddrBook::Address.](iaddrbook-address.md)</span><span class="sxs-lookup"><span data-stu-id="5f4a4-136">Consequently, a pointer to a handle should not be expected in the  _lpulUIParam_ parameter of [IAddrBook::Address](iaddrbook-address.md).</span></span>
    
<span data-ttu-id="5f4a4-137">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-137">**lpReserved**</span></span>
  
> <span data-ttu-id="5f4a4-138">Зарезервировано, должно быть ноль.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-138">Reserved, must be zero.</span></span>
    
<span data-ttu-id="5f4a4-139">**ulHelpContext**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-139">**ulHelpContext**</span></span>
  
> <span data-ttu-id="5f4a4-140">Указывает контекст в **справке,** который сначала будет показан при нажатии кнопки справки в диалоговом окне адресов.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-140">Specifies the context within **Help** that will first be shown when the user clicks the Help button in the address dialog box.</span></span> 
    
<span data-ttu-id="5f4a4-141">**lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-141">**lpszHelpFileName**</span></span>
  
> <span data-ttu-id="5f4a4-142">Указатель на имя файла справки, который будет связан с диалоговое окно адреса.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-142">Pointer to the name of a Help file that will be associated with the address dialog box.</span></span> <span data-ttu-id="5f4a4-143">Член **lpszHelpFileName** используется вместе с **ulHelpContext** для вызова функции **Windows WinHelp.**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-143">The **lpszHelpFileName** member is used together with **ulHelpContext** to call the Windows **WinHelp** function.</span></span> 
    
<span data-ttu-id="5f4a4-144">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-144">**lpfnABSDI**</span></span>
  
> <span data-ttu-id="5f4a4-145">Указатель на функцию MAPI на основе прототипа [ACCELERATEABSDI](accelerateabsdi.md) или NULL.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-145">Pointer to a MAPI function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype or NULL.</span></span> <span data-ttu-id="5f4a4-146">Этот член применяется только к безмежной версии диалогового окна, как указывается в заданной DIALOG_SDI флаге.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-146">This member applies to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="5f4a4-147">Клиенты, строив структуру **ADRPARM** для переададновки [в IAddrBook::Address,](iaddrbook-address.md) всегда должны задать **члену lpfnABSDI** NULL.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-147">Clients building an **ADRPARM** structure to pass to [IAddrBook::Address](iaddrbook-address.md) must always set the **lpfnABSDI** member to NULL.</span></span> <span data-ttu-id="5f4a4-148">Если флаг DIALOG_SDI, MAPI закажит его в допустимую функцию перед возвращением.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-148">If the DIALOG_SDI flag is set, MAPI will then set it to a valid function before returning.</span></span> <span data-ttu-id="5f4a4-149">Клиенты называют эту функцию из цикла сообщений, чтобы убедиться, что ускорители в диалоговом окне адресной книги работают.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-149">Clients call this function from in their message loop to make sure that accelerators in the address book dialog box work.</span></span> <span data-ttu-id="5f4a4-150">При отклонении диалогового окна и вызове функции MAPI, на которые указывает член **lpfnDismiss,** клиенты должны отогнать функцию **ACCELERATEABSDI** из цикла сообщений.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-150">When the dialog box is dismissed and MAPI calls the function pointed to by the **lpfnDismiss** member, clients should unhook the **ACCELERATEABSDI** function from their message loop.</span></span> 
    
<span data-ttu-id="5f4a4-151">**lpfnDismiss**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-151">**lpfnDismiss**</span></span>
  
> <span data-ttu-id="5f4a4-152">Указатель на функцию на основе прототипа [DISMISSMODELESS](dismissmodeless.md) или NULL.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-152">Pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype or NULL.</span></span> <span data-ttu-id="5f4a4-153">Этот член применяется только к безмежной версии диалогового окна, как указывается в заданной DIALOG_SDI флаге.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-153">This member applies only to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="5f4a4-154">MAPI вызывает функцию **DISMISSMODELESS,** когда пользователь отклонять диалоговое окно без режима адреса, информируя клиента, вызываемого **IAddrBook::Address,** что диалоговое окно больше не активна.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-154">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client calling **IAddrBook::Address** that the dialog box is no longer active.</span></span> 
    
<span data-ttu-id="5f4a4-155">**lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-155">**lpvDismissContext**</span></span>
  
> <span data-ttu-id="5f4a4-156">Указатель для контекстной информации, которая будет передана функции **DISMISSMODELESS,** указываемой участником **lpfnDismiss.**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-156">Pointer to context information to be passed to the **DISMISSMODELESS** function pointed to by the **lpfnDismiss** member.</span></span> <span data-ttu-id="5f4a4-157">Этот член применяется только к безмежной версии диалогового окна, как указывается в заданной DIALOG_SDI флаге.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-157">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> 
    
<span data-ttu-id="5f4a4-158">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-158">**lpszCaption**</span></span>
  
> <span data-ttu-id="5f4a4-159">Указатель на текст, который будет использоваться в качестве заголовка для общего диалогового окна адресов.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-159">Pointer to text to be used as the title for the common address dialog box.</span></span>
    
<span data-ttu-id="5f4a4-160">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-160">**lpszNewEntryTitle**</span></span>
  
> <span data-ttu-id="5f4a4-161">Указатель на текст, который будет использоваться в качестве метки кнопки для кнопки, вызываемой диалогового окна **New Entry** или другого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-161">Pointer to text to be used as the button label for the button that invokes either the **New Entry** dialog box or another dialog box.</span></span> 
    
<span data-ttu-id="5f4a4-162">**lpszDestWellsTitle**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-162">**lpszDestWellsTitle**</span></span>
  
> <span data-ttu-id="5f4a4-163">Указатель на текст, который будет использоваться в качестве заголовка для элементов управления текстовым полем получателя, которые могут отображаться в модальной версии диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-163">Pointer to text to be used as a title for the recipient text box controls that can appear in the modal version of the common address dialog box.</span></span> <span data-ttu-id="5f4a4-164">Этот член не используется для бес режимных диалогов.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-164">This member is not used for modeless dialog boxes.</span></span> 
    
<span data-ttu-id="5f4a4-165">**cDestFields**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-165">**cDestFields**</span></span>
  
> <span data-ttu-id="5f4a4-166">Количество элементов управления текстовым полем получателей в модальной версии диалогового окна адреса или нулевое значение, если диалоговое окно является бес режимным.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-166">Count of recipient text box controls in the modal version of the address dialog box, or zero if the dialog box is modeless.</span></span> <span data-ttu-id="5f4a4-167">Диалоговое окно адресов открыто для просмотра только при следующих условиях:</span><span class="sxs-lookup"><span data-stu-id="5f4a4-167">The address dialog box is open for browsing only when the following conditions are true:</span></span> 
    
  - <span data-ttu-id="5f4a4-168">Значение **участника cDestFields** установлено до нуля.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-168">The **cDestFields** member is set to zero.</span></span> 
    
  - <span data-ttu-id="5f4a4-169">Установлен DIALOG_BOX флаг.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-169">The DIALOG_BOX flag is set.</span></span>
    
  - <span data-ttu-id="5f4a4-170">Флаг ADDRESS_ONE не установлен.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-170">The ADDRESS_ONE flag is not set.</span></span>
    
  <span data-ttu-id="5f4a4-171">Настройка **cDestFields** для 0XFFFFFFFF означает, что MAPI должна создать по умолчанию число элементов управления текстовыми полями получателей.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-171">Setting **cDestFields** to 0XFFFFFFFF implies that MAPI should create the default number of recipient text box controls.</span></span> <span data-ttu-id="5f4a4-172">В этом случае **участниками lppszDestTitles** и **lpulDestComps** должны быть NULL.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-172">In this case, the **lppszDestTitles** and **lpulDestComps** members must be NULL.</span></span> 
    
<span data-ttu-id="5f4a4-173">**nDestFieldFocus**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-173">**nDestFieldFocus**</span></span>
  
> <span data-ttu-id="5f4a4-174">Указывает определенное управление текстовым полем, которое должно иметь начальное внимание при отывке модальной версии диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-174">Indicates the particular text box control that should have the initial focus when the modal version of the dialog box appears.</span></span> <span data-ttu-id="5f4a4-175">Это значение должно быть от 0 до значения **cDestFields** минус 1.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-175">This value must be between 0 and the value of **cDestFields** minus 1.</span></span> 
    
<span data-ttu-id="5f4a4-176">**lppszDestTitles**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-176">**lppszDestTitles**</span></span>
  
> <span data-ttu-id="5f4a4-177">Указатель на массив меток для кнопок, связанных с каждым из элементов управления текстовым полем, отображаемого в модальной версии диалогового окна адреса.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-177">Pointer to an array of labels for buttons associated with each of the text box controls that are displayed in the modal version of the address dialog box.</span></span> <span data-ttu-id="5f4a4-178">Значение члена **cDestFields** указывает количество меток, включенных в массив.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-178">The value of the **cDestFields** member indicates the number of labels included in the array.</span></span> <span data-ttu-id="5f4a4-179">Если участником **lppszDestTitles** является NULL, метод **Address** использует названия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-179">If the **lppszDestTitles** member is NULL, the **Address** method uses default titles.</span></span> 
    
<span data-ttu-id="5f4a4-180">**lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-180">**lpulDestComps**</span></span>
  
> <span data-ttu-id="5f4a4-181">Указатель на массив значений типа получателей, таких как MAPI_TO, MAPI_CC и MAPI_BCC, связанный с каждым управлением текстовым полем.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-181">Pointer to an array of recipient type values, such as MAPI_TO, MAPI_CC, and MAPI_BCC, that is associated with each text box control.</span></span> <span data-ttu-id="5f4a4-182">Значение члена **CDestFields** указывает количество типов получателей, включенных в массив.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-182">The value of the **CDestFields** member indicates the number of recipient types included in the array.</span></span> <span data-ttu-id="5f4a4-183">Значения, на которые указывают **lpulDestComps,** можно  использовать для PR_RECIPIENT_TYPE [(PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)свойства каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-183">The values pointed to by **lpulDestComps** can be used to set the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property of each recipient.</span></span> <span data-ttu-id="5f4a4-184">Если участником **lpulDestComps** является NULL, метод **Address** использует типы получателей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-184">If the **lpulDestComps** member is NULL, the **Address** method uses default recipient types.</span></span> 
    
<span data-ttu-id="5f4a4-185">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-185">**lpContRestriction**</span></span>
  
> <span data-ttu-id="5f4a4-186">Указатель на [структуру SRestriction,](srestriction.md) которая ограничивает тип записей адресов, которые могут отображаться в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-186">Pointer to an [SRestriction](srestriction.md) structure that limits the type of address entries that can be displayed in the dialog box.</span></span> 
    
<span data-ttu-id="5f4a4-187">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-187">**lpHierRestriction**</span></span>
  
> <span data-ttu-id="5f4a4-188">Указатель на **структуру SRestriction,** которая ограничивает контейнеры адресной книги, которые могут поставлять записи адресов для отображения в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-188">Pointer to an **SRestriction** structure that limits the address book containers that can supply address entries to be displayed in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5f4a4-189">Примечания</span><span class="sxs-lookup"><span data-stu-id="5f4a4-189">Remarks</span></span>

<span data-ttu-id="5f4a4-190">**Структуры ADRPARM** используются клиентами и поставщиками услуг для контроля внешнего вида и поведения диалоговых окне общего адреса MAPI.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-190">**ADRPARM** structures are used by clients and service providers to control the appearance and behavior of the MAPI common address dialog boxes.</span></span> <span data-ttu-id="5f4a4-191">Существует два варианта диалоговых окне адресов: modeless и modal.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-191">There are two varieties of the address dialog box: modeless and modal.</span></span> <span data-ttu-id="5f4a4-192">Некоторые члены в структуре **ADRPARM** применяются к обеим версиям диалогового окна, но некоторые применяются только к одной из двух версий.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-192">Some of the members in the **ADRPARM** structure apply to both versions of the dialog box, but some only apply to one of the two versions.</span></span> <span data-ttu-id="5f4a4-193">В следующей таблице участники структуры **ADRPARM** связаны с их использованием с общими диалогами адресов.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-193">The following table relates the members of an **ADRPARM** structure to their use with the common address dialog boxes.</span></span> 
  
|<span data-ttu-id="5f4a4-194">Член ADRPARM</span><span class="sxs-lookup"><span data-stu-id="5f4a4-194">ADRPARM member</span></span>|<span data-ttu-id="5f4a4-195">Тип диалоговое окно</span><span class="sxs-lookup"><span data-stu-id="5f4a4-195">Type of dialog box</span></span>|
|:-----|:-----|
|<span data-ttu-id="5f4a4-196">**cbABContEntryID** и **lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-196">**cbABContEntryID** and **lpABContEntryID**</span></span> <br/> |<span data-ttu-id="5f4a4-197">Modal и modeless</span><span class="sxs-lookup"><span data-stu-id="5f4a4-197">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="5f4a4-198">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-198">**ulFlags**</span></span> <br/> |<span data-ttu-id="5f4a4-199">Modal и modeless</span><span class="sxs-lookup"><span data-stu-id="5f4a4-199">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="5f4a4-200">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-200">**lpReserved**</span></span> <br/> |<span data-ttu-id="5f4a4-201">Modal и modeless</span><span class="sxs-lookup"><span data-stu-id="5f4a4-201">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="5f4a4-202">**ulHelpContext и** **lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-202">**ulHelpContext** and **lpszHelpFileName**</span></span> <br/> |<span data-ttu-id="5f4a4-203">Modal и modeless</span><span class="sxs-lookup"><span data-stu-id="5f4a4-203">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="5f4a4-204">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-204">**lpfnABSDI**</span></span> <br/> |<span data-ttu-id="5f4a4-205">Modeless</span><span class="sxs-lookup"><span data-stu-id="5f4a4-205">Modeless</span></span>  <br/> |
|<span data-ttu-id="5f4a4-206">**lpfnDismiss** и **lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-206">**lpfnDismiss** and **lpvDismissContext**</span></span> <br/> |<span data-ttu-id="5f4a4-207">Modeless</span><span class="sxs-lookup"><span data-stu-id="5f4a4-207">Modeless</span></span>  <br/> |
|<span data-ttu-id="5f4a4-208">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-208">**lpszCaption**</span></span> <br/> |<span data-ttu-id="5f4a4-209">Modal и modeless</span><span class="sxs-lookup"><span data-stu-id="5f4a4-209">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="5f4a4-210">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-210">**lpszNewEntryTitle**</span></span> <br/> |<span data-ttu-id="5f4a4-211">Модальный</span><span class="sxs-lookup"><span data-stu-id="5f4a4-211">Modal</span></span>  <br/> |
|<span data-ttu-id="5f4a4-212">**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles** и **lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-212">**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**, and **lpulDestComps**</span></span> <br/> |<span data-ttu-id="5f4a4-213">Модальный</span><span class="sxs-lookup"><span data-stu-id="5f4a4-213">Modal</span></span>  <br/> |
|<span data-ttu-id="5f4a4-214">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-214">**lpContRestriction**</span></span> <br/> |<span data-ttu-id="5f4a4-215">Modal и modeless</span><span class="sxs-lookup"><span data-stu-id="5f4a4-215">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="5f4a4-216">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-216">**lpHierRestriction**</span></span> <br/> |<span data-ttu-id="5f4a4-217">Modal и modeless</span><span class="sxs-lookup"><span data-stu-id="5f4a4-217">Modal and modeless</span></span>  <br/> |
   
<span data-ttu-id="5f4a4-218">Диалоговое окно без режима — это отображение записей из одного или более контейнеров адресной книги только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-218">The modeless dialog box is a read-only display of entries from one or more address book containers.</span></span> <span data-ttu-id="5f4a4-219">Диалоговое окно может отображать все записи из выбранных контейнеров или ограничиваться только теми записями и контейнерами, которые соответствуют критериям, установленным ограничением.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-219">The dialog box can display all entries from the selected containers or be limited to only those entries and containers that match criteria established by a restriction.</span></span> <span data-ttu-id="5f4a4-220">Ограничение содержимого, на которое указывает **lpContRestriction,** может ограничить типы отображаемой записи, а ограничение иерархии, на которое указывает **lpHierRestriction,** может ограничить контейнеры, предоставляющие записи.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-220">The contents restriction pointed to by **lpContRestriction** can limit the types of entries displayed and the hierarchy restriction pointed to by **lpHierRestriction** can limit the containers providing the entries.</span></span> <span data-ttu-id="5f4a4-221">Чтобы сообщить звониму об отклонении диалогового окна, MAPI вызывает функцию, предоставляемую вызываемой вызываемой, которая соответствует [прототипу DISMISSMODELESS.](dismissmodeless.md)</span><span class="sxs-lookup"><span data-stu-id="5f4a4-221">To inform the caller when the dialog box is dismissed, MAPI invokes a function that is provided by the caller that matches the [DISMISSMODELESS](dismissmodeless.md) prototype.</span></span> <span data-ttu-id="5f4a4-222">Другая функция, которая соответствует прототипу [ACCELERATEABSDI,](accelerateabsdi.md) предоставляется MAPI и вызывается вызываемой вызываемой в цикле сообщений Windows для облегчения работы клавишных ярлыков.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-222">Another function, one that matches the [ACCELERATEABSDI](accelerateabsdi.md) prototype, is provided by MAPI and invoked by the caller in the Windows message loop to facilitate the working of keyboard shortcuts.</span></span> <span data-ttu-id="5f4a4-223">Бесхозяйная версия диалогового окна адреса MAPI может отображаться, когда клиенты звонят [в IAddrBook::Address](iaddrbook-address.md) или когда поставщики услуг называют [IMAPISupport::Address.](imapisupport-address.md)</span><span class="sxs-lookup"><span data-stu-id="5f4a4-223">The modeless version of the MAPI address dialog box can be displayed when clients call [IAddrBook::Address](iaddrbook-address.md) or when service providers call [IMAPISupport::Address](imapisupport-address.md).</span></span> 
  
<span data-ttu-id="5f4a4-224">Диалоговое окно modal — это отображение записей из одного или более контейнеров.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-224">The modal dialog box is a read/write display of entries from one or more containers.</span></span> <span data-ttu-id="5f4a4-225">Его содержимое может быть затронуто таким же образом, как и в бесконтактной версии ограничениями, установленными в **членах lpContRestriction** и **lpHierRestriction.**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-225">Its contents can be affected in the same manner as the modeless version by restrictions set in the **lpContRestriction** and **lpHierRestriction** members.</span></span> <span data-ttu-id="5f4a4-226">Помимо окна списка, отображаемого записей контейнера, диалоговое окно modal может содержать от одного до трех элементов управления текстовым полем для хранения записей, выбранных пользователем.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-226">In addition to the list box displaying container entries, the modal dialog box can contain between one and three text box controls for holding entries selected by the user.</span></span> <span data-ttu-id="5f4a4-227">Каждый контроль редактирования связан с определенным типом **получателя или PR_RECIPIENT_TYPE,** например MAPI_TO.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-227">Each edit control is associated with a particular recipient type or **PR_RECIPIENT_TYPE** property such as MAPI_TO.</span></span> <span data-ttu-id="5f4a4-228">Диалоговое окно модального адреса может отображаться  с помощью методов Адрес или когда клиенты звонят [в IAddrBook::D etails,](iaddrbook-details.md) а поставщики услуг называют [IMAPISupport::D etails](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="5f4a4-228">The modal address dialog box can be displayed by either of the **Address** methods or when clients call [IAddrBook::Details](iaddrbook-details.md) and service providers call [IMAPISupport::Details](imapisupport-details.md).</span></span> 
  
<span data-ttu-id="5f4a4-229">Эта иллюстрация включает два управления текстовым полем, так как член **cDestFields** структуры **ADRPARM,** контролирующей отображение этого диалогового окна, задает 2.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-229">This illustration includes two text box controls because the **cDestFields** member of the **ADRPARM** structure controlling the display of this dialog box is set to 2.</span></span> <span data-ttu-id="5f4a4-230">Первый контроль имеет начальное внимание, так как для **члена nDestFieldFocus** установлено 0.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-230">The first control has initial focus because the **nDestFieldFocus** member is set to 0.</span></span> 
  
<span data-ttu-id="5f4a4-231">Член **lpszNewEntryTitle** указывает на текст для метки кнопки, которая при выборе вызывает отображение дополнительного диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-231">The **lpszNewEntryTitle** member points to text for a button label that, when it is selected, causes an additional dialog box to be displayed.</span></span> <span data-ttu-id="5f4a4-232">Как правило, как показано на иллюстрации диалогового окна modal, кнопка помечена New, а в диалоговом окне, которое отображается, перечислены все типы адресов, которые могут быть созданы любыми поставщиками адресных книг в профиле. </span><span class="sxs-lookup"><span data-stu-id="5f4a4-232">Typically, as is shown in the illustration of the modal dialog box, the button is labeled **New** and the dialog box that appears lists all of the types of addresses that can be created by any of the address book providers in the profile.</span></span> <span data-ttu-id="5f4a4-233">Клиенты вызывают отображение этого диалогового окна New **Entry,** вызывая [параметр IAddrBook::NewEntry](iaddrbook-newentry.md) и продавая ноль для параметра  _cbEidNewEntryTpl_ и NULL для  _параметра lpEidNewEntryTpl_ при выборе кнопки.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-233">Clients cause this **New Entry** dialog box to be displayed by calling [IAddrBook::NewEntry](iaddrbook-newentry.md) and passing zero for the  _cbEidNewEntryTpl_ parameter and NULL for the  _lpEidNewEntryTpl_ parameter when the user selects the button.</span></span> <span data-ttu-id="5f4a4-234">Сведения, включенные в диалоговое окно, приходят из разной таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-234">The information that is included in this dialog box comes from the MAPI one-off table.</span></span> 
  
<span data-ttu-id="5f4a4-235">Каждая запись в этом диалоговом окне связана с шаблоном ввода данных, необходимых для создания адреса определенного типа.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-235">Every entry in this dialog box is associated with a template for entering the data required to create an address of the particular type.</span></span> <span data-ttu-id="5f4a4-236">Большинство поставщиков адресных книг поставляют по одному шаблону для каждого типа записи адреса, которую они могут создать.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-236">Most address book providers supply one template for every type of address entry they can create.</span></span> <span data-ttu-id="5f4a4-237">Когда пользователь делает выбор из этого диалогового окна, MAPI отображает соответствующий шаблон.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-237">When a user makes a selection from this dialog box, MAPI displays the corresponding template.</span></span>
  
<span data-ttu-id="5f4a4-238">Наиболее значительные четыре бита члена **ulFlags** структуры **ADRPARM** содержат номер версии, определяющий версию **структуры ADRPARM.**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-238">The most significant four bits of the **ADRPARM** structure's **ulFlags** member contain a version number identifying the version of the **ADRPARM** structure.</span></span> <span data-ttu-id="5f4a4-239">Текущая версия — 0 (ноль) или ADRPARM_HELP_CTX.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-239">The current version is 0 (zero) or ADRPARM_HELP_CTX.</span></span> <span data-ttu-id="5f4a4-240">Текущая реализация MAPI будет неудачной для любой версии структуры, кроме нуля.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-240">The current implementation of MAPI will fail for any version of the structure other than zero.</span></span> 
  
<span data-ttu-id="5f4a4-241">Будущие версии структуры могут быть совершенно другими; они могут не поддерживать структуру version-zero.</span><span class="sxs-lookup"><span data-stu-id="5f4a4-241">Future versions of the structure may be completely different; they may not support the version-zero structure.</span></span> <span data-ttu-id="5f4a4-242">Для извлечения номера версии из члена **ulFlags** и объединения его с определенными флагами предоставляются следующие макрос:</span><span class="sxs-lookup"><span data-stu-id="5f4a4-242">The following macros are provided for extracting the version number from the **ulFlags** member and for combining it with the defined flags:</span></span> 
  
- <span data-ttu-id="5f4a4-243">**GET_ADRPARM_VERSION** _(ulFlags)_</span><span class="sxs-lookup"><span data-stu-id="5f4a4-243">**GET_ADRPARM_VERSION** (_ulFlags_)</span></span> 
- <span data-ttu-id="5f4a4-244">**SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _)</span><span class="sxs-lookup"><span data-stu-id="5f4a4-244">**SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _)</span></span> 
- <span data-ttu-id="5f4a4-245">**ADRPARM_HELP_CTX**</span><span class="sxs-lookup"><span data-stu-id="5f4a4-245">**ADRPARM_HELP_CTX**</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5f4a4-246">См. также</span><span class="sxs-lookup"><span data-stu-id="5f4a4-246">See also</span></span>

- [<span data-ttu-id="5f4a4-247">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="5f4a4-247">ACCELERATEABSDI</span></span>](accelerateabsdi.md)
- [<span data-ttu-id="5f4a4-248">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="5f4a4-248">DISMISSMODELESS</span></span>](dismissmodeless.md)
- [<span data-ttu-id="5f4a4-249">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="5f4a4-249">IAddrBook::Address</span></span>](iaddrbook-address.md)
- [<span data-ttu-id="5f4a4-250">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="5f4a4-250">IMAPISupport::Address</span></span>](imapisupport-address.md)
- [<span data-ttu-id="5f4a4-251">SRestriction</span><span class="sxs-lookup"><span data-stu-id="5f4a4-251">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="5f4a4-252">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="5f4a4-252">MAPI Structures</span></span>](mapi-structures.md)

