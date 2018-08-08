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
ms.openlocfilehash: ad26cb9b77404d6470f7a8d787eb85edc5cce402
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2018
ms.locfileid: "19808044"
---
# <a name="adrparm"></a><span data-ttu-id="27289-103">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="27289-103">ADRPARM</span></span>

<span data-ttu-id="27289-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27289-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27289-105">Описание отображения и поведения стандартным диалоговым окном адрес.</span><span class="sxs-lookup"><span data-stu-id="27289-105">Describes the display and behavior of the common address dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27289-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="27289-106">Header file:</span></span>  <br/> |<span data-ttu-id="27289-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27289-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="27289-108">Members</span><span class="sxs-lookup"><span data-stu-id="27289-108">Members</span></span>

<span data-ttu-id="27289-109">**cbABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="27289-109">**cbABContEntryID**</span></span>
  
> <span data-ttu-id="27289-110">Число байт в идентификаторе запись, на который указывает **lpABContEntryID**.</span><span class="sxs-lookup"><span data-stu-id="27289-110">Count of bytes in the entry identifier pointed to by **lpABContEntryID**.</span></span>
    
<span data-ttu-id="27289-111">**lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="27289-111">**lpABContEntryID**</span></span>
  
> <span data-ttu-id="27289-112">Указатель на идентификатор записи контейнера, представляющий начальное список адресов получателей, которые отображаются в поле адрес.</span><span class="sxs-lookup"><span data-stu-id="27289-112">Pointer to the entry identifier of the container that supplies the initial list of recipient addresses that are displayed in the address dialog box.</span></span>
    
<span data-ttu-id="27289-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="27289-113">**ulFlags**</span></span>
  
> <span data-ttu-id="27289-114">Битовая маска флаги, связанные с различные параметры диалогового окна адрес.</span><span class="sxs-lookup"><span data-stu-id="27289-114">Bitmask of flags associated with various address dialog box options.</span></span> <span data-ttu-id="27289-115">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="27289-115">The following flags can be set:</span></span>
    
<span data-ttu-id="27289-116">AB_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="27289-116">AB_RESOLVE</span></span>
  
> <span data-ttu-id="27289-117">Включите все имена разрешаться после закрытия диалогового окна адрес.</span><span class="sxs-lookup"><span data-stu-id="27289-117">Enable all names to be resolved after the address dialog box is closed.</span></span> <span data-ttu-id="27289-118">В случае неоднозначные операций, которые возникают из процесса разрешения имен диалоговое окно отображается для запроса пользователя для получения справки по их устранению.</span><span class="sxs-lookup"><span data-stu-id="27289-118">If there are ambiguous entries that result from the name resolution process, a dialog box appears to prompt the user for help in resolving them.</span></span> <span data-ttu-id="27289-119">Параметр, этот флаг гарантирует, что все имена, возвращаемые [IAddrBook::Address](iaddrbook-address.md) разрешаются.</span><span class="sxs-lookup"><span data-stu-id="27289-119">Setting this flag guarantees that all of the names returned by [IAddrBook::Address](iaddrbook-address.md) are resolved.</span></span> 
    
<span data-ttu-id="27289-120">AB_SELECTONLY</span><span class="sxs-lookup"><span data-stu-id="27289-120">AB_SELECTONLY</span></span>
  
> <span data-ttu-id="27289-121">Отключение создания одноразовых адреса для списка получателей.</span><span class="sxs-lookup"><span data-stu-id="27289-121">Disable the creation of one-off addresses for a recipient list.</span></span> <span data-ttu-id="27289-122">Этот флаг используется только в том случае, если окно является модальным, как указанной флагом DIALOG_MODAL задаваемая.</span><span class="sxs-lookup"><span data-stu-id="27289-122">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span>
    
<span data-ttu-id="27289-123">ADDRESS_ONE</span><span class="sxs-lookup"><span data-stu-id="27289-123">ADDRESS_ONE</span></span>
  
> <span data-ttu-id="27289-124">Пользователь может выбрать только один получатель вместо нескольким получателям из списка.</span><span class="sxs-lookup"><span data-stu-id="27289-124">The user can select exactly one recipient instead of multiple recipients from a list.</span></span> <span data-ttu-id="27289-125">Этот флаг действителен только в том случае, если **cDestFields** равно 0, а диалоговое окно является модальным, как указанной флагом DIALOG_MODAL задаваемая.</span><span class="sxs-lookup"><span data-stu-id="27289-125">This flag is valid only when **cDestFields** is zero and the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="27289-126">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="27289-126">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="27289-127">Вызывает модальное версии общие адреса диалогового окна для отображения.</span><span class="sxs-lookup"><span data-stu-id="27289-127">Causes the modal version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="27289-128">Необходимо задать этот флаг или DIALOG_SDI; они не могут быть заданы.</span><span class="sxs-lookup"><span data-stu-id="27289-128">Either this flag or DIALOG_SDI should be set; they cannot both be set.</span></span> 
    
<span data-ttu-id="27289-129">DIALOG_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="27289-129">DIALOG_OPTIONS</span></span>
  
> <span data-ttu-id="27289-130">Вызывает кнопки **Отправить параметры** для отображения в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="27289-130">Causes the **Send Options** button to be displayed in the dialog box.</span></span> <span data-ttu-id="27289-131">Этот флаг используется только в том случае, если окно является модальным, как указанной флагом DIALOG_MODAL задаваемая.</span><span class="sxs-lookup"><span data-stu-id="27289-131">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="27289-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="27289-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="27289-133">Вызывает безрежимным версии общие адреса диалогового окна для отображения.</span><span class="sxs-lookup"><span data-stu-id="27289-133">Causes the modeless version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="27289-134">Необходимо задать этот флаг или DIALOG_MODAL; они не могут быть заданы.</span><span class="sxs-lookup"><span data-stu-id="27289-134">Either this flag or DIALOG_MODAL should be set; they cannot both be set.</span></span> <span data-ttu-id="27289-135">Флаг DIALOG_SDI игнорируется для клиентов, не являющиеся Outlook и будет отображаться версия модального диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="27289-135">The DIALOG_SDI flag is ignored for non-Outlook clients, and the modal version of the dialog box will be displayed.</span></span> <span data-ttu-id="27289-136">Следовательно указатель мыши на маркер не следует ожидать в параметре _lpulUIParam_ [IAddrBook::Address](iaddrbook-address.md).</span><span class="sxs-lookup"><span data-stu-id="27289-136">Consequently, a pointer to a handle should not be expected in the  _lpulUIParam_ parameter of [IAddrBook::Address](iaddrbook-address.md).</span></span>
    
<span data-ttu-id="27289-137">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="27289-137">**lpReserved**</span></span>
  
> <span data-ttu-id="27289-138">Зарезервированные, должен быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="27289-138">Reserved, must be zero.</span></span>
    
<span data-ttu-id="27289-139">**ulHelpContext**</span><span class="sxs-lookup"><span data-stu-id="27289-139">**ulHelpContext**</span></span>
  
> <span data-ttu-id="27289-140">Определяет контекст, в рамках **справки** , который будет отображаться сначала при нажатии кнопки справки в поле адрес.</span><span class="sxs-lookup"><span data-stu-id="27289-140">Specifies the context within **Help** that will first be shown when the user clicks the Help button in the address dialog box.</span></span> 
    
<span data-ttu-id="27289-141">**lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="27289-141">**lpszHelpFileName**</span></span>
  
> <span data-ttu-id="27289-142">Указатель на имя файла справки, который будет связан с диалоговое окно "адрес".</span><span class="sxs-lookup"><span data-stu-id="27289-142">Pointer to the name of a Help file that will be associated with the address dialog box.</span></span> <span data-ttu-id="27289-143">Член **lpszHelpFileName** используется вместе с **ulHelpContext** для вызова функции Windows **WinHelp** .</span><span class="sxs-lookup"><span data-stu-id="27289-143">The **lpszHelpFileName** member is used together with **ulHelpContext** to call the Windows **WinHelp** function.</span></span> 
    
<span data-ttu-id="27289-144">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="27289-144">**lpfnABSDI**</span></span>
  
> <span data-ttu-id="27289-145">Указатель на функцию MAPI на основе прототип [ACCELERATEABSDI](accelerateabsdi.md) или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="27289-145">Pointer to a MAPI function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype or NULL.</span></span> <span data-ttu-id="27289-146">Этот член относится к безрежимным версии диалоговое окно, только как указанной флагом DIALOG_SDI задаваемая.</span><span class="sxs-lookup"><span data-stu-id="27289-146">This member applies to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="27289-147">Построение структуру **ADRPARM** для передачи [IAddrBook::Address](iaddrbook-address.md) клиентов должны всегда набора **lpfnABSDI** значение NULL.</span><span class="sxs-lookup"><span data-stu-id="27289-147">Clients building an **ADRPARM** structure to pass to [IAddrBook::Address](iaddrbook-address.md) must always set the **lpfnABSDI** member to NULL.</span></span> <span data-ttu-id="27289-148">Если значение флага DIALOG_SDI, MAPI будет установите его в допустимую функцию перед возвращением.</span><span class="sxs-lookup"><span data-stu-id="27289-148">If the DIALOG_SDI flag is set, MAPI will then set it to a valid function before returning.</span></span> <span data-ttu-id="27289-149">Клиенты эта функция из в их цикл обработки сообщений, чтобы убедиться в том, что ускорители работы в поле адрес книги рабочих поле диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="27289-149">Clients call this function from in their message loop to make sure that accelerators in the address book dialog box work.</span></span> <span data-ttu-id="27289-150">При закрытии диалоговое окно MAPI вызывает функцию, на который указывает член **lpfnDismiss** , клиенты должны отсоедините функцию **ACCELERATEABSDI** из своих цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="27289-150">When the dialog box is dismissed and MAPI calls the function pointed to by the **lpfnDismiss** member, clients should unhook the **ACCELERATEABSDI** function from their message loop.</span></span> 
    
<span data-ttu-id="27289-151">**lpfnDismiss**</span><span class="sxs-lookup"><span data-stu-id="27289-151">**lpfnDismiss**</span></span>
  
> <span data-ttu-id="27289-152">Указатель на функцию на основе прототип [DISMISSMODELESS](dismissmodeless.md) или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="27289-152">Pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype or NULL.</span></span> <span data-ttu-id="27289-153">Этот член применим только к безрежимным версии диалоговое окно, только как указанной флагом DIALOG_SDI задаваемая.</span><span class="sxs-lookup"><span data-stu-id="27289-153">This member applies only to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="27289-154">MAPI вызывает **DISMISSMODELESS** функцию, если пользователь не закрывает диалоговое окно безрежимным адрес, уведомляющее о клиента, вызывающего **IAddrBook::Address** диалоговое окно не является активной.</span><span class="sxs-lookup"><span data-stu-id="27289-154">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client calling **IAddrBook::Address** that the dialog box is no longer active.</span></span> 
    
<span data-ttu-id="27289-155">**lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="27289-155">**lpvDismissContext**</span></span>
  
> <span data-ttu-id="27289-156">Указатель на данные контекста, передаваемых в функцию **DISMISSMODELESS** , на который указывает член **lpfnDismiss** .</span><span class="sxs-lookup"><span data-stu-id="27289-156">Pointer to context information to be passed to the **DISMISSMODELESS** function pointed to by the **lpfnDismiss** member.</span></span> <span data-ttu-id="27289-157">Этот член применим только к безрежимным версии диалоговом окне, указанной флагом DIALOG_SDI задаваемая.</span><span class="sxs-lookup"><span data-stu-id="27289-157">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> 
    
<span data-ttu-id="27289-158">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="27289-158">**lpszCaption**</span></span>
  
> <span data-ttu-id="27289-159">Указатель на текст, который используется в качестве названия для стандартным диалоговым окном адрес.</span><span class="sxs-lookup"><span data-stu-id="27289-159">Pointer to text to be used as the title for the common address dialog box.</span></span>
    
<span data-ttu-id="27289-160">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="27289-160">**lpszNewEntryTitle**</span></span>
  
> <span data-ttu-id="27289-161">Указатель на текст для использования в качестве метки кнопки для кнопки, который вызывает диалоговое окно **Новая запись** или другое диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="27289-161">Pointer to text to be used as the button label for the button that invokes either the **New Entry** dialog box or another dialog box.</span></span> 
    
<span data-ttu-id="27289-162">**lpszDestWellsTitle**</span><span class="sxs-lookup"><span data-stu-id="27289-162">**lpszDestWellsTitle**</span></span>
  
> <span data-ttu-id="27289-163">Указатель на текст для использования в качестве заголовка для получателей элемента управления текстовых полей, которые могут появляться в модальное версии стандартным диалоговым окном адрес.</span><span class="sxs-lookup"><span data-stu-id="27289-163">Pointer to text to be used as a title for the recipient text box controls that can appear in the modal version of the common address dialog box.</span></span> <span data-ttu-id="27289-164">Этот член не используется для безрежимным диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="27289-164">This member is not used for modeless dialog boxes.</span></span> 
    
<span data-ttu-id="27289-165">**cDestFields**</span><span class="sxs-lookup"><span data-stu-id="27289-165">**cDestFields**</span></span>
  
> <span data-ttu-id="27289-166">Число получателей текстовых полей в версии модальное диалоговое окно "адрес" или ноль, если окно является безрежимным.</span><span class="sxs-lookup"><span data-stu-id="27289-166">Count of recipient text box controls in the modal version of the address dialog box, or zero if the dialog box is modeless.</span></span> <span data-ttu-id="27289-167">Диалоговое окно "адрес" Открыть для просмотра только в том случае, если выполняются следующие условия:</span><span class="sxs-lookup"><span data-stu-id="27289-167">The address dialog box is open for browsing only when the following conditions are true:</span></span> 
    
  - <span data-ttu-id="27289-168">Член **cDestFields** присваивается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="27289-168">The **cDestFields** member is set to zero.</span></span> 
    
  - <span data-ttu-id="27289-169">Флаг DIALOG_BOX установлен.</span><span class="sxs-lookup"><span data-stu-id="27289-169">The DIALOG_BOX flag is set.</span></span>
    
  - <span data-ttu-id="27289-170">Флаг ADDRESS_ONE не установлен.</span><span class="sxs-lookup"><span data-stu-id="27289-170">The ADDRESS_ONE flag is not set.</span></span>
    
  <span data-ttu-id="27289-171">Установка **cDestFields** для 0XFFFFFFFF предполагает, что MAPI следует создать по умолчанию число получателей текст элемента управления полей.</span><span class="sxs-lookup"><span data-stu-id="27289-171">Setting **cDestFields** to 0XFFFFFFFF implies that MAPI should create the default number of recipient text box controls.</span></span> <span data-ttu-id="27289-172">В этом случае члены **lppszDestTitles** и **lpulDestComps** значения NULL.</span><span class="sxs-lookup"><span data-stu-id="27289-172">In this case, the **lppszDestTitles** and **lpulDestComps** members must be NULL.</span></span> 
    
<span data-ttu-id="27289-173">**nDestFieldFocus**</span><span class="sxs-lookup"><span data-stu-id="27289-173">**nDestFieldFocus**</span></span>
  
> <span data-ttu-id="27289-174">Указывает, определенного текстового поля, для которого следует внимание при отображении версии модального диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="27289-174">Indicates the particular text box control that should have the initial focus when the modal version of the dialog box appears.</span></span> <span data-ttu-id="27289-175">Это значение должно быть между 0 и значением **cDestFields** минус 1.</span><span class="sxs-lookup"><span data-stu-id="27289-175">This value must be between 0 and the value of **cDestFields** minus 1.</span></span> 
    
<span data-ttu-id="27289-176">**lppszDestTitles**</span><span class="sxs-lookup"><span data-stu-id="27289-176">**lppszDestTitles**</span></span>
  
> <span data-ttu-id="27289-177">Указатель на массив метки для кнопки, связанные с каждым из элемента управления текстовых полей, отображаемых в версию модальное диалоговое окно "адрес".</span><span class="sxs-lookup"><span data-stu-id="27289-177">Pointer to an array of labels for buttons associated with each of the text box controls that are displayed in the modal version of the address dialog box.</span></span> <span data-ttu-id="27289-178">Значение элемента **cDestFields** указывает число меток, включенные в массиве.</span><span class="sxs-lookup"><span data-stu-id="27289-178">The value of the **cDestFields** member indicates the number of labels included in the array.</span></span> <span data-ttu-id="27289-179">Если член **lppszDestTitles** имеет значение NULL, метод **адрес** использует по умолчанию заголовков.</span><span class="sxs-lookup"><span data-stu-id="27289-179">If the **lppszDestTitles** member is NULL, the **Address** method uses default titles.</span></span> 
    
<span data-ttu-id="27289-180">**lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="27289-180">**lpulDestComps**</span></span>
  
> <span data-ttu-id="27289-181">Указатель на массив значений тип получателя, например MAPI_TO, MAPI_CC и MAPI_BCC, который связан с каждой текстового поля.</span><span class="sxs-lookup"><span data-stu-id="27289-181">Pointer to an array of recipient type values, such as MAPI_TO, MAPI_CC, and MAPI_BCC, that is associated with each text box control.</span></span> <span data-ttu-id="27289-182">Значение элемента **CDestFields** показывает, сколько типов получателей, включенных в массиве.</span><span class="sxs-lookup"><span data-stu-id="27289-182">The value of the **CDestFields** member indicates the number of recipient types included in the array.</span></span> <span data-ttu-id="27289-183">Значения, на который указывает **lpulDestComps** можно использовать для свойства **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="27289-183">The values pointed to by **lpulDestComps** can be used to set the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property of each recipient.</span></span> <span data-ttu-id="27289-184">Если член **lpulDestComps** имеет значение NULL, метод **адрес** использует типы получателей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="27289-184">If the **lpulDestComps** member is NULL, the **Address** method uses default recipient types.</span></span> 
    
<span data-ttu-id="27289-185">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="27289-185">**lpContRestriction**</span></span>
  
> <span data-ttu-id="27289-186">Указатель на структуру [SRestriction](srestriction.md) , какие записей адресов, которые могут отображаться в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="27289-186">Pointer to an [SRestriction](srestriction.md) structure that limits the type of address entries that can be displayed in the dialog box.</span></span> 
    
<span data-ttu-id="27289-187">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="27289-187">**lpHierRestriction**</span></span>
  
> <span data-ttu-id="27289-188">Указатель на структуру **SRestriction** , которая ограничивает контейнеров адресной книги, которые можно предоставить записей адресов для отображения в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="27289-188">Pointer to an **SRestriction** structure that limits the address book containers that can supply address entries to be displayed in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="27289-189">Замечания</span><span class="sxs-lookup"><span data-stu-id="27289-189">Remarks</span></span>

<span data-ttu-id="27289-190">**ADRPARM** структуры используются для управления внешний вид и поведение MAPI адрес окон с клиентов и поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="27289-190">**ADRPARM** structures are used by clients and service providers to control the appearance and behavior of the MAPI common address dialog boxes.</span></span> <span data-ttu-id="27289-191">Существуют два вида диалоговое окно "адрес": безрежимным и модальные окна.</span><span class="sxs-lookup"><span data-stu-id="27289-191">There are two varieties of the address dialog box: modeless and modal.</span></span> <span data-ttu-id="27289-192">Некоторые элементы в структуре **ADRPARM** применяются для обеих версий диалоговое окно, но некоторые применимы только к одной из двух версий.</span><span class="sxs-lookup"><span data-stu-id="27289-192">Some of the members in the **ADRPARM** structure apply to both versions of the dialog box, but some only apply to one of the two versions.</span></span> <span data-ttu-id="27289-193">В следующей таблице элементы структуры **ADRPARM** относится к их использования с адреса окон.</span><span class="sxs-lookup"><span data-stu-id="27289-193">The following table relates the members of an **ADRPARM** structure to their use with the common address dialog boxes.</span></span> 
  
|<span data-ttu-id="27289-194">Член ADRPARM</span><span class="sxs-lookup"><span data-stu-id="27289-194">ADRPARM member</span></span>|<span data-ttu-id="27289-195">Тип диалогового окна</span><span class="sxs-lookup"><span data-stu-id="27289-195">Type of dialog box</span></span>|
|:-----|:-----|
|<span data-ttu-id="27289-196">**cbABContEntryID** и **lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="27289-196">**cbABContEntryID** and **lpABContEntryID**</span></span> <br/> |<span data-ttu-id="27289-197">Модальные окна и безрежимным</span><span class="sxs-lookup"><span data-stu-id="27289-197">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="27289-198">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="27289-198">**ulFlags**</span></span> <br/> |<span data-ttu-id="27289-199">Модальные окна и безрежимным</span><span class="sxs-lookup"><span data-stu-id="27289-199">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="27289-200">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="27289-200">**lpReserved**</span></span> <br/> |<span data-ttu-id="27289-201">Модальные окна и безрежимным</span><span class="sxs-lookup"><span data-stu-id="27289-201">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="27289-202">**ulHelpContext** и **lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="27289-202">**ulHelpContext** and **lpszHelpFileName**</span></span> <br/> |<span data-ttu-id="27289-203">Модальные окна и безрежимным</span><span class="sxs-lookup"><span data-stu-id="27289-203">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="27289-204">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="27289-204">**lpfnABSDI**</span></span> <br/> |<span data-ttu-id="27289-205">MODELESS</span><span class="sxs-lookup"><span data-stu-id="27289-205">Modeless</span></span>  <br/> |
|<span data-ttu-id="27289-206">**lpfnDismiss** и **lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="27289-206">**lpfnDismiss** and **lpvDismissContext**</span></span> <br/> |<span data-ttu-id="27289-207">MODELESS</span><span class="sxs-lookup"><span data-stu-id="27289-207">Modeless</span></span>  <br/> |
|<span data-ttu-id="27289-208">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="27289-208">**lpszCaption**</span></span> <br/> |<span data-ttu-id="27289-209">Модальные окна и безрежимным</span><span class="sxs-lookup"><span data-stu-id="27289-209">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="27289-210">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="27289-210">**lpszNewEntryTitle**</span></span> <br/> |<span data-ttu-id="27289-211">Модальные окна</span><span class="sxs-lookup"><span data-stu-id="27289-211">Modal</span></span>  <br/> |
|<span data-ttu-id="27289-212">**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**и **lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="27289-212">**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**, and **lpulDestComps**</span></span> <br/> |<span data-ttu-id="27289-213">Модальные окна</span><span class="sxs-lookup"><span data-stu-id="27289-213">Modal</span></span>  <br/> |
|<span data-ttu-id="27289-214">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="27289-214">**lpContRestriction**</span></span> <br/> |<span data-ttu-id="27289-215">Модальные окна и безрежимным</span><span class="sxs-lookup"><span data-stu-id="27289-215">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="27289-216">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="27289-216">**lpHierRestriction**</span></span> <br/> |<span data-ttu-id="27289-217">Модальные окна и безрежимным</span><span class="sxs-lookup"><span data-stu-id="27289-217">Modal and modeless</span></span>  <br/> |
   
<span data-ttu-id="27289-218">Диалоговое окно безрежимным отображается только для чтения записей из одного или нескольких контейнеров адресной книги.</span><span class="sxs-lookup"><span data-stu-id="27289-218">The modeless dialog box is a read-only display of entries from one or more address book containers.</span></span> <span data-ttu-id="27289-219">Диалоговое окно можно отобразить все записи из выбранного контейнеров или ограничиваться записей и контейнеры, которые соответствуют критериям, приведенным в ограничение.</span><span class="sxs-lookup"><span data-stu-id="27289-219">The dialog box can display all entries from the selected containers or be limited to only those entries and containers that match criteria established by a restriction.</span></span> <span data-ttu-id="27289-220">Ограничение содержимое, на который указывает **lpContRestriction** можно ограничить типы записей отображаются и ограничения иерархии, на который указывает **lpHierRestriction** можно ограничить контейнеров, предоставляя записей.</span><span class="sxs-lookup"><span data-stu-id="27289-220">The contents restriction pointed to by **lpContRestriction** can limit the types of entries displayed and the hierarchy restriction pointed to by **lpHierRestriction** can limit the containers providing the entries.</span></span> <span data-ttu-id="27289-221">Для оповещения вызывающего абонента, когда диалоговое окно закрывается, MAPI вызывает функцию, предоставленные вызывающего абонента, которая соответствует прототип [DISMISSMODELESS](dismissmodeless.md) .</span><span class="sxs-lookup"><span data-stu-id="27289-221">To inform the caller when the dialog box is dismissed, MAPI invokes a function that is provided by the caller that matches the [DISMISSMODELESS](dismissmodeless.md) prototype.</span></span> <span data-ttu-id="27289-222">Другой функции, соответствующий прототип [ACCELERATEABSDI](accelerateabsdi.md) , автор MAPI и вызывать вызывающим абонентом в цикл обработки сообщений Windows, чтобы облегчить работу сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="27289-222">Another function, one that matches the [ACCELERATEABSDI](accelerateabsdi.md) prototype, is provided by MAPI and invoked by the caller in the Windows message loop to facilitate the working of keyboard shortcuts.</span></span> <span data-ttu-id="27289-223">Когда клиенты вызывать [IAddrBook::Address](iaddrbook-address.md) или [IMAPISupport::Address](imapisupport-address.md)вызова поставщиков услуг отображается безрежимным версия MAPI адреса диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="27289-223">The modeless version of the MAPI address dialog box can be displayed when clients call [IAddrBook::Address](iaddrbook-address.md) or when service providers call [IMAPISupport::Address](imapisupport-address.md).</span></span> 
  
<span data-ttu-id="27289-224">Чтение и запись модального диалогового окна отображается записей из одного или нескольких контейнеров.</span><span class="sxs-lookup"><span data-stu-id="27289-224">The modal dialog box is a read/write display of entries from one or more containers.</span></span> <span data-ttu-id="27289-225">Его содержимое может измениться точно так же, безрежимным версии путем ограничения установки в **lpContRestriction** и **lpHierRestriction** элементы.</span><span class="sxs-lookup"><span data-stu-id="27289-225">Its contents can be affected in the same manner as the modeless version by restrictions set in the **lpContRestriction** and **lpHierRestriction** members.</span></span> <span data-ttu-id="27289-226">В дополнение к поле со списком отображения элементов контейнера модального диалогового окна может содержать от одного до трех элемента управления текстовых полей для хранения записей, выбранный пользователем.</span><span class="sxs-lookup"><span data-stu-id="27289-226">In addition to the list box displaying container entries, the modal dialog box can contain between one and three text box controls for holding entries selected by the user.</span></span> <span data-ttu-id="27289-227">Все элементы управления, изменить связан с определенным типом получателей или **PR_RECIPIENT_TYPE** свойства, такие как MAPI_TO.</span><span class="sxs-lookup"><span data-stu-id="27289-227">Each edit control is associated with a particular recipient type or **PR_RECIPIENT_TYPE** property such as MAPI_TO.</span></span> <span data-ttu-id="27289-228">Диалоговое окно модальное адрес отображаются с помощью одного из методов **адрес** или при клиенты вызывать [IAddrBook::Details](iaddrbook-details.md) и [IMAPISupport::Details](imapisupport-details.md)вызова поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="27289-228">The modal address dialog box can be displayed by either of the **Address** methods or when clients call [IAddrBook::Details](iaddrbook-details.md) and service providers call [IMAPISupport::Details](imapisupport-details.md).</span></span> 
  
<span data-ttu-id="27289-229">На этом рисунке включает в себя два элемента управления текстовых полей так, как член **cDestFields** структуры **ADRPARM** , управление отображением в этом диалоговом окне 2.</span><span class="sxs-lookup"><span data-stu-id="27289-229">This illustration includes two text box controls because the **cDestFields** member of the **ADRPARM** structure controlling the display of this dialog box is set to 2.</span></span> <span data-ttu-id="27289-230">Первый элемент управления имеет фокус начального, так как член **nDestFieldFocus** имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="27289-230">The first control has initial focus because the **nDestFieldFocus** member is set to 0.</span></span> 
  
<span data-ttu-id="27289-231">Элемент **lpszNewEntryTitle** указывает текст для метки кнопки, выполнение, при этом дополнительное диалоговое для отображения.</span><span class="sxs-lookup"><span data-stu-id="27289-231">The **lpszNewEntryTitle** member points to text for a button label that, when it is selected, causes an additional dialog box to be displayed.</span></span> <span data-ttu-id="27289-232">Как правило как показано на рисунке модального диалогового окна, кнопка помечена как **Создать** и поле, которое отображается список всех типов адресов, которые могут быть созданы в указанных поставщиками адресной книги в профиле.</span><span class="sxs-lookup"><span data-stu-id="27289-232">Typically, as is shown in the illustration of the modal dialog box, the button is labeled **New** and the dialog box that appears lists all of the types of addresses that can be created by any of the address book providers in the profile.</span></span> <span data-ttu-id="27289-233">Клиенты вызвать это диалоговое окно **Новая запись** будет отображаться путем вызова [IAddrBook::NewEntry](iaddrbook-newentry.md) и передачи нуля для параметра _cbEidNewEntryTpl_ и значение NULL для параметра _lpEidNewEntryTpl_ при выборе пользователем кнопки.</span><span class="sxs-lookup"><span data-stu-id="27289-233">Clients cause this **New Entry** dialog box to be displayed by calling [IAddrBook::NewEntry](iaddrbook-newentry.md) and passing zero for the  _cbEidNewEntryTpl_ parameter and NULL for the  _lpEidNewEntryTpl_ parameter when the user selects the button.</span></span> <span data-ttu-id="27289-234">Сведения, содержащиеся в данном диалоговом извлекаются из таблицы одноразовых MAPI.</span><span class="sxs-lookup"><span data-stu-id="27289-234">The information that is included in this dialog box comes from the MAPI one-off table.</span></span> 
  
<span data-ttu-id="27289-235">Каждая запись в данном диалоговом связан с шаблоном для ввода данных, необходимых для создания адрес определенного типа.</span><span class="sxs-lookup"><span data-stu-id="27289-235">Every entry in this dialog box is associated with a template for entering the data required to create an address of the particular type.</span></span> <span data-ttu-id="27289-236">Большинство поставщиками адресной книги всегда один шаблон для каждого типа записи адресов, которые они могут быть созданы.</span><span class="sxs-lookup"><span data-stu-id="27289-236">Most address book providers supply one template for every type of address entry they can create.</span></span> <span data-ttu-id="27289-237">Когда пользователь выбирает элемент в этом диалоговом окне, MAPI отображает соответствующий шаблон.</span><span class="sxs-lookup"><span data-stu-id="27289-237">When a user makes a selection from this dialog box, MAPI displays the corresponding template.</span></span>
  
<span data-ttu-id="27289-238">Наиболее важные четыре бита член **ulFlags** структуры **ADRPARM** содержат версии номер, идентифицирующий версию структуры **ADRPARM** .</span><span class="sxs-lookup"><span data-stu-id="27289-238">The most significant four bits of the **ADRPARM** structure's **ulFlags** member contain a version number identifying the version of the **ADRPARM** structure.</span></span> <span data-ttu-id="27289-239">Текущая версия равно 0 (нулю) или ADRPARM_HELP_CTX.</span><span class="sxs-lookup"><span data-stu-id="27289-239">The current version is 0 (zero) or ADRPARM_HELP_CTX.</span></span> <span data-ttu-id="27289-240">Текущая реализация интерфейса MAPI завершится с ошибкой для любой версии структуры, отличное от нуля.</span><span class="sxs-lookup"><span data-stu-id="27289-240">The current implementation of MAPI will fail for any version of the structure other than zero.</span></span> 
  
<span data-ttu-id="27289-241">Будущих версий структуры может быть заменено другим; они могут не поддерживать Структура версии нулю.</span><span class="sxs-lookup"><span data-stu-id="27289-241">Future versions of the structure may be completely different; they may not support the version-zero structure.</span></span> <span data-ttu-id="27289-242">Для извлечения из члена **ulFlags** номер версии, а также для объединения с определенных флагов предоставляются следующие макросы:</span><span class="sxs-lookup"><span data-stu-id="27289-242">The following macros are provided for extracting the version number from the **ulFlags** member and for combining it with the defined flags:</span></span> 
  
- <span data-ttu-id="27289-243">**GET_ADRPARM_VERSION** (_ulFlags_)</span><span class="sxs-lookup"><span data-stu-id="27289-243">**GET_ADRPARM_VERSION** (_ulFlags_)</span></span> 
- <span data-ttu-id="27289-244">**SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _)</span><span class="sxs-lookup"><span data-stu-id="27289-244">**SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _)</span></span> 
- <span data-ttu-id="27289-245">**ADRPARM_HELP_CTX**</span><span class="sxs-lookup"><span data-stu-id="27289-245">**ADRPARM_HELP_CTX**</span></span>
  
## <a name="see-also"></a><span data-ttu-id="27289-246">См. также</span><span class="sxs-lookup"><span data-stu-id="27289-246">See also</span></span>

- [<span data-ttu-id="27289-247">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="27289-247">ACCELERATEABSDI</span></span>](accelerateabsdi.md)
- [<span data-ttu-id="27289-248">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="27289-248">DISMISSMODELESS</span></span>](dismissmodeless.md)
- [<span data-ttu-id="27289-249">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="27289-249">IAddrBook::Address</span></span>](iaddrbook-address.md)
- [<span data-ttu-id="27289-250">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="27289-250">IMAPISupport::Address</span></span>](imapisupport-address.md)
- [<span data-ttu-id="27289-251">SRestriction</span><span class="sxs-lookup"><span data-stu-id="27289-251">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="27289-252">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="27289-252">MAPI Structures</span></span>](mapi-structures.md)

