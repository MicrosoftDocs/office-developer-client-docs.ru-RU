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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330221"
---
# <a name="adrparm"></a><span data-ttu-id="4c060-103">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="4c060-103">ADRPARM</span></span>

<span data-ttu-id="4c060-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c060-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c060-105">Описывает отображение и поведение диалогового окна "общий адрес".</span><span class="sxs-lookup"><span data-stu-id="4c060-105">Describes the display and behavior of the common address dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c060-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4c060-106">Header file:</span></span>  <br/> |<span data-ttu-id="4c060-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="4c060-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="4c060-108">Members</span><span class="sxs-lookup"><span data-stu-id="4c060-108">Members</span></span>

<span data-ttu-id="4c060-109">**Кбабконтентрид**</span><span class="sxs-lookup"><span data-stu-id="4c060-109">**cbABContEntryID**</span></span>
  
> <span data-ttu-id="4c060-110">Количество байтов в идентификаторе записи, на который указывает **лпабконтентрид**.</span><span class="sxs-lookup"><span data-stu-id="4c060-110">Count of bytes in the entry identifier pointed to by **lpABContEntryID**.</span></span>
    
<span data-ttu-id="4c060-111">**Лпабконтентрид**</span><span class="sxs-lookup"><span data-stu-id="4c060-111">**lpABContEntryID**</span></span>
  
> <span data-ttu-id="4c060-112">Указатель на идентификатор записи контейнера, который предоставляет начальный список адресов получателей, отображаемых в диалоговом окне адрес.</span><span class="sxs-lookup"><span data-stu-id="4c060-112">Pointer to the entry identifier of the container that supplies the initial list of recipient addresses that are displayed in the address dialog box.</span></span>
    
<span data-ttu-id="4c060-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="4c060-113">**ulFlags**</span></span>
  
> <span data-ttu-id="4c060-114">Битовая маска флагов, связанных с различными параметрами диалогового окна адреса.</span><span class="sxs-lookup"><span data-stu-id="4c060-114">Bitmask of flags associated with various address dialog box options.</span></span> <span data-ttu-id="4c060-115">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="4c060-115">The following flags can be set:</span></span>
    
<span data-ttu-id="4c060-116">АБ_РЕСОЛВЕ</span><span class="sxs-lookup"><span data-stu-id="4c060-116">AB_RESOLVE</span></span>
  
> <span data-ttu-id="4c060-117">Включите разрешение всех имен после закрытия диалогового окна "адрес".</span><span class="sxs-lookup"><span data-stu-id="4c060-117">Enable all names to be resolved after the address dialog box is closed.</span></span> <span data-ttu-id="4c060-118">При наличии неоднозначных записей, которые могут возникать в процессе разрешения имен, отображается диалоговое окно с запросом на помощь пользователю при их разрешении.</span><span class="sxs-lookup"><span data-stu-id="4c060-118">If there are ambiguous entries that result from the name resolution process, a dialog box appears to prompt the user for help in resolving them.</span></span> <span data-ttu-id="4c060-119">Установка этого флага гарантирует, что все имена, возвращаемые методом [IAddrBook:: Address](iaddrbook-address.md) , будут разрешены.</span><span class="sxs-lookup"><span data-stu-id="4c060-119">Setting this flag guarantees that all of the names returned by [IAddrBook::Address](iaddrbook-address.md) are resolved.</span></span> 
    
<span data-ttu-id="4c060-120">АБ_СЕЛЕКТОНЛИ</span><span class="sxs-lookup"><span data-stu-id="4c060-120">AB_SELECTONLY</span></span>
  
> <span data-ttu-id="4c060-121">Отключение создания одноразовых адресов для списка получателей.</span><span class="sxs-lookup"><span data-stu-id="4c060-121">Disable the creation of one-off addresses for a recipient list.</span></span> <span data-ttu-id="4c060-122">Этот флаг используется только в том случае, если диалоговое окно является модальным, как показано в заданном флаге ДИАЛОГ_МОДАЛ.</span><span class="sxs-lookup"><span data-stu-id="4c060-122">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span>
    
<span data-ttu-id="4c060-123">АДДРЕСС_ОНЕ</span><span class="sxs-lookup"><span data-stu-id="4c060-123">ADDRESS_ONE</span></span>
  
> <span data-ttu-id="4c060-124">Пользователь может выбрать только одного получателя, а не нескольких получателей в списке.</span><span class="sxs-lookup"><span data-stu-id="4c060-124">The user can select exactly one recipient instead of multiple recipients from a list.</span></span> <span data-ttu-id="4c060-125">Этот флаг действителен, только если **кдестфиелдс** имеет значение 0, а диалоговое окно является модальным, как показано в заданном флаге диалог_модал.</span><span class="sxs-lookup"><span data-stu-id="4c060-125">This flag is valid only when **cDestFields** is zero and the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="4c060-126">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="4c060-126">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="4c060-127">Вызывает отображение модальной версии диалогового окна Общий адрес.</span><span class="sxs-lookup"><span data-stu-id="4c060-127">Causes the modal version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="4c060-128">Этот флаг или ДИАЛОГ_СДИ должен быть задан; они не могут быть заданы одновременно.</span><span class="sxs-lookup"><span data-stu-id="4c060-128">Either this flag or DIALOG_SDI should be set; they cannot both be set.</span></span> 
    
<span data-ttu-id="4c060-129">ДИАЛОГ_ОПТИОНС</span><span class="sxs-lookup"><span data-stu-id="4c060-129">DIALOG_OPTIONS</span></span>
  
> <span data-ttu-id="4c060-130">Вызывает отображение кнопки " **Параметры отправки** " в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="4c060-130">Causes the **Send Options** button to be displayed in the dialog box.</span></span> <span data-ttu-id="4c060-131">Этот флаг используется только в том случае, если диалоговое окно является модальным, как показано в заданном флаге ДИАЛОГ_МОДАЛ.</span><span class="sxs-lookup"><span data-stu-id="4c060-131">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="4c060-132">ДИАЛОГ_СДИ</span><span class="sxs-lookup"><span data-stu-id="4c060-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="4c060-133">Приводит к отображению немодальной версии диалогового окна Общий адрес.</span><span class="sxs-lookup"><span data-stu-id="4c060-133">Causes the modeless version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="4c060-134">Этот флаг или ДИАЛОГ_МОДАЛ должен быть задан; они не могут быть заданы одновременно.</span><span class="sxs-lookup"><span data-stu-id="4c060-134">Either this flag or DIALOG_MODAL should be set; they cannot both be set.</span></span> <span data-ttu-id="4c060-135">Флаг ДИАЛОГ_СДИ игнорируется для клиентов, отличных от Outlook, и отображается модальная версия диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4c060-135">The DIALOG_SDI flag is ignored for non-Outlook clients, and the modal version of the dialog box will be displayed.</span></span> <span data-ttu-id="4c060-136">Поэтому указатель на дескриптор не должен быть ожидаемым в параметре _лпулуипарам_ объекта [IAddrBook:: Address](iaddrbook-address.md).</span><span class="sxs-lookup"><span data-stu-id="4c060-136">Consequently, a pointer to a handle should not be expected in the  _lpulUIParam_ parameter of [IAddrBook::Address](iaddrbook-address.md).</span></span>
    
<span data-ttu-id="4c060-137">**Лпресервед**</span><span class="sxs-lookup"><span data-stu-id="4c060-137">**lpReserved**</span></span>
  
> <span data-ttu-id="4c060-138">ЗаРезервировано, должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="4c060-138">Reserved, must be zero.</span></span>
    
<span data-ttu-id="4c060-139">**Улхелпконтекст**</span><span class="sxs-lookup"><span data-stu-id="4c060-139">**ulHelpContext**</span></span>
  
> <span data-ttu-id="4c060-140">Задает контекст в **справке** , который будет отображаться при нажатии пользователем кнопки Справка в диалоговом окне адрес.</span><span class="sxs-lookup"><span data-stu-id="4c060-140">Specifies the context within **Help** that will first be shown when the user clicks the Help button in the address dialog box.</span></span> 
    
<span data-ttu-id="4c060-141">**Лпсзелпфиленаме**</span><span class="sxs-lookup"><span data-stu-id="4c060-141">**lpszHelpFileName**</span></span>
  
> <span data-ttu-id="4c060-142">Указатель на имя файла справки, который будет связан с диалоговым окном "адрес".</span><span class="sxs-lookup"><span data-stu-id="4c060-142">Pointer to the name of a Help file that will be associated with the address dialog box.</span></span> <span data-ttu-id="4c060-143">Элемент **лпсзелпфиленаме** используется вместе с **улхелпконтекст** для вызова функции Windows **WinHelp** .</span><span class="sxs-lookup"><span data-stu-id="4c060-143">The **lpszHelpFileName** member is used together with **ulHelpContext** to call the Windows **WinHelp** function.</span></span> 
    
<span data-ttu-id="4c060-144">**Лпфнабсди**</span><span class="sxs-lookup"><span data-stu-id="4c060-144">**lpfnABSDI**</span></span>
  
> <span data-ttu-id="4c060-145">Указатель на функцию MAPI на основе прототипа [акцелератеабсди](accelerateabsdi.md) или значения NULL.</span><span class="sxs-lookup"><span data-stu-id="4c060-145">Pointer to a MAPI function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype or NULL.</span></span> <span data-ttu-id="4c060-146">Этот член применяется только к немодальной версии диалогового окна, как указано в установленном флаге ДИАЛОГ_СДИ.</span><span class="sxs-lookup"><span data-stu-id="4c060-146">This member applies to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="4c060-147">Клиенты, создающие структуру **адрпарм** для передачи в [IAddrBook:: Address](iaddrbook-address.md) должен всегда приСвоить элементу **лпфнабсди** значение null.</span><span class="sxs-lookup"><span data-stu-id="4c060-147">Clients building an **ADRPARM** structure to pass to [IAddrBook::Address](iaddrbook-address.md) must always set the **lpfnABSDI** member to NULL.</span></span> <span data-ttu-id="4c060-148">Если установлен флаг ДИАЛОГ_СДИ, MAPI задаст для него допустимую функцию, прежде чем возвратить значение.</span><span class="sxs-lookup"><span data-stu-id="4c060-148">If the DIALOG_SDI flag is set, MAPI will then set it to a valid function before returning.</span></span> <span data-ttu-id="4c060-149">Клиенты вызывают эту функцию из цикла сообщений, чтобы убедиться, что ускорители в диалоговом окне Адресная книга работают.</span><span class="sxs-lookup"><span data-stu-id="4c060-149">Clients call this function from in their message loop to make sure that accelerators in the address book dialog box work.</span></span> <span data-ttu-id="4c060-150">Когда диалоговое окно закрывается, а MAPI вызывает функцию, на которую ссылается член **лпфндисмисс** , клиенты должны отсоединить функцию **акцелератеабсди** от своего цикла обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="4c060-150">When the dialog box is dismissed and MAPI calls the function pointed to by the **lpfnDismiss** member, clients should unhook the **ACCELERATEABSDI** function from their message loop.</span></span> 
    
<span data-ttu-id="4c060-151">**Лпфндисмисс**</span><span class="sxs-lookup"><span data-stu-id="4c060-151">**lpfnDismiss**</span></span>
  
> <span data-ttu-id="4c060-152">Указатель на функцию на основе прототипа [дисмиссмоделесс](dismissmodeless.md) или значение null.</span><span class="sxs-lookup"><span data-stu-id="4c060-152">Pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype or NULL.</span></span> <span data-ttu-id="4c060-153">Этот элемент применяется только к немодальной версии диалогового окна, как указано в установленном флаге ДИАЛОГ_СДИ.</span><span class="sxs-lookup"><span data-stu-id="4c060-153">This member applies only to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="4c060-154">MAPI вызывает функцию **дисмиссмоделесс** , когда пользователь закрывает диалоговое окно с немодальным адресом, что информирует клиентский вызов **IAddrBook:: адрес** , который больше не активен в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="4c060-154">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client calling **IAddrBook::Address** that the dialog box is no longer active.</span></span> 
    
<span data-ttu-id="4c060-155">**Лпвдисмиссконтекст**</span><span class="sxs-lookup"><span data-stu-id="4c060-155">**lpvDismissContext**</span></span>
  
> <span data-ttu-id="4c060-156">Указатель на сведения контекста, передаваемые в функцию **дисмиссмоделесс** , на которую указывает элемент **лпфндисмисс** .</span><span class="sxs-lookup"><span data-stu-id="4c060-156">Pointer to context information to be passed to the **DISMISSMODELESS** function pointed to by the **lpfnDismiss** member.</span></span> <span data-ttu-id="4c060-157">Этот элемент применяется только к немодальной версии диалогового окна, как указано в установленном флаге ДИАЛОГ_СДИ.</span><span class="sxs-lookup"><span data-stu-id="4c060-157">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> 
    
<span data-ttu-id="4c060-158">**Лпсзкаптион**</span><span class="sxs-lookup"><span data-stu-id="4c060-158">**lpszCaption**</span></span>
  
> <span data-ttu-id="4c060-159">Указатель на текст, который будет использоваться в качестве заголовка для диалогового окна "общий адрес".</span><span class="sxs-lookup"><span data-stu-id="4c060-159">Pointer to text to be used as the title for the common address dialog box.</span></span>
    
<span data-ttu-id="4c060-160">**Лпсзневентрититле**</span><span class="sxs-lookup"><span data-stu-id="4c060-160">**lpszNewEntryTitle**</span></span>
  
> <span data-ttu-id="4c060-161">Указатель на текст, который будет использоваться в качестве подписи кнопки, которая вызывает диалоговое окно " **создать запись** " или другое диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4c060-161">Pointer to text to be used as the button label for the button that invokes either the **New Entry** dialog box or another dialog box.</span></span> 
    
<span data-ttu-id="4c060-162">**Лпсздествеллститле**</span><span class="sxs-lookup"><span data-stu-id="4c060-162">**lpszDestWellsTitle**</span></span>
  
> <span data-ttu-id="4c060-163">Указатель на текст, который будет использоваться в качестве заголовка для элементов управления текстовым полем получателя, которые могут отображаться в модальной версии диалогового окна Общий адрес.</span><span class="sxs-lookup"><span data-stu-id="4c060-163">Pointer to text to be used as a title for the recipient text box controls that can appear in the modal version of the common address dialog box.</span></span> <span data-ttu-id="4c060-164">Этот элемент не используется для немодальных диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="4c060-164">This member is not used for modeless dialog boxes.</span></span> 
    
<span data-ttu-id="4c060-165">**Кдестфиелдс**</span><span class="sxs-lookup"><span data-stu-id="4c060-165">**cDestFields**</span></span>
  
> <span data-ttu-id="4c060-166">Количество элементов управления текстовым полем "получатель" в модальной версии диалогового окна "адрес" или ноль, если диалоговое окно является немодальным.</span><span class="sxs-lookup"><span data-stu-id="4c060-166">Count of recipient text box controls in the modal version of the address dialog box, or zero if the dialog box is modeless.</span></span> <span data-ttu-id="4c060-167">Диалоговое окно адрес открыто только для просмотра при соблюдении следующих условий:</span><span class="sxs-lookup"><span data-stu-id="4c060-167">The address dialog box is open for browsing only when the following conditions are true:</span></span> 
    
  - <span data-ttu-id="4c060-168">Для члена **кдестфиелдс** задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="4c060-168">The **cDestFields** member is set to zero.</span></span> 
    
  - <span data-ttu-id="4c060-169">Установлен флаг ДИАЛОГ_БОКС.</span><span class="sxs-lookup"><span data-stu-id="4c060-169">The DIALOG_BOX flag is set.</span></span>
    
  - <span data-ttu-id="4c060-170">Флаг АДДРЕСС_ОНЕ не установлен.</span><span class="sxs-lookup"><span data-stu-id="4c060-170">The ADDRESS_ONE flag is not set.</span></span>
    
  <span data-ttu-id="4c060-171">Если для параметра **Кдестфиелдс** задано значение 0XFFFFFFFF, MAPI должен создать количество элементов управления текстовым полем получателя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4c060-171">Setting **cDestFields** to 0XFFFFFFFF implies that MAPI should create the default number of recipient text box controls.</span></span> <span data-ttu-id="4c060-172">В этом случае члены **лппсздесттитлес** и **ЛПУЛДЕСТКОМПС** должны иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="4c060-172">In this case, the **lppszDestTitles** and **lpulDestComps** members must be NULL.</span></span> 
    
<span data-ttu-id="4c060-173">**Ндестфиелдфокус**</span><span class="sxs-lookup"><span data-stu-id="4c060-173">**nDestFieldFocus**</span></span>
  
> <span data-ttu-id="4c060-174">Указывает конкретное текстовое поле, которое должно иметь начальный фокус при появлении модальной версии диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4c060-174">Indicates the particular text box control that should have the initial focus when the modal version of the dialog box appears.</span></span> <span data-ttu-id="4c060-175">Это значение должно находиться в диапазоне от 0 до значения **кдестфиелдс** минус 1.</span><span class="sxs-lookup"><span data-stu-id="4c060-175">This value must be between 0 and the value of **cDestFields** minus 1.</span></span> 
    
<span data-ttu-id="4c060-176">**Лппсздесттитлес**</span><span class="sxs-lookup"><span data-stu-id="4c060-176">**lppszDestTitles**</span></span>
  
> <span data-ttu-id="4c060-177">Указатель на массив меток для кнопок, связанных с каждым из элементов управления текстовым полем, которые отображаются в модальной версии диалогового окна "адрес".</span><span class="sxs-lookup"><span data-stu-id="4c060-177">Pointer to an array of labels for buttons associated with each of the text box controls that are displayed in the modal version of the address dialog box.</span></span> <span data-ttu-id="4c060-178">Значение элемента **кдестфиелдс** указывает количество меток, включенных в массив.</span><span class="sxs-lookup"><span data-stu-id="4c060-178">The value of the **cDestFields** member indicates the number of labels included in the array.</span></span> <span data-ttu-id="4c060-179">Если элемент **лппсздесттитлес** имеет значение null, метод **Address** использует названия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4c060-179">If the **lppszDestTitles** member is NULL, the **Address** method uses default titles.</span></span> 
    
<span data-ttu-id="4c060-180">**Лпулдесткомпс**</span><span class="sxs-lookup"><span data-stu-id="4c060-180">**lpulDestComps**</span></span>
  
> <span data-ttu-id="4c060-181">Указатель на массив значений типов получателей, таких как МАПИ_ТО, МАПИ_КК и МАПИ_БКК, связанный с каждым элементом управления "текстовое поле".</span><span class="sxs-lookup"><span data-stu-id="4c060-181">Pointer to an array of recipient type values, such as MAPI_TO, MAPI_CC, and MAPI_BCC, that is associated with each text box control.</span></span> <span data-ttu-id="4c060-182">Значение элемента **кдестфиелдс** указывает количество типов получателей, включенных в массив.</span><span class="sxs-lookup"><span data-stu-id="4c060-182">The value of the **CDestFields** member indicates the number of recipient types included in the array.</span></span> <span data-ttu-id="4c060-183">Значения, указываемые в **лпулдесткомпс** , можно использовать для установки свойства **пр_реЦипиент_типе** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="4c060-183">The values pointed to by **lpulDestComps** can be used to set the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property of each recipient.</span></span> <span data-ttu-id="4c060-184">Если элемент **лпулдесткомпс** имеет значение null, метод **Address** использует типы получателей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4c060-184">If the **lpulDestComps** member is NULL, the **Address** method uses default recipient types.</span></span> 
    
<span data-ttu-id="4c060-185">**Лпконтрестриктион**</span><span class="sxs-lookup"><span data-stu-id="4c060-185">**lpContRestriction**</span></span>
  
> <span data-ttu-id="4c060-186">Указатель на структуру [срестриктион](srestriction.md) , которая ограничит тип записей адресов, которые могут отображаться в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="4c060-186">Pointer to an [SRestriction](srestriction.md) structure that limits the type of address entries that can be displayed in the dialog box.</span></span> 
    
<span data-ttu-id="4c060-187">**Лфиеррестриктион**</span><span class="sxs-lookup"><span data-stu-id="4c060-187">**lpHierRestriction**</span></span>
  
> <span data-ttu-id="4c060-188">Указатель на структуру **срестриктион** , ограничивающую контейнеры адресных книг, которые могут предоставлять записи адресов для отображения в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="4c060-188">Pointer to an **SRestriction** structure that limits the address book containers that can supply address entries to be displayed in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4c060-189">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c060-189">Remarks</span></span>

<span data-ttu-id="4c060-190">Структуры **адрпарм** используются клиентами и поставщиками услуг для управления внешним видом и поведением диалоговых окон общего адреса MAPI.</span><span class="sxs-lookup"><span data-stu-id="4c060-190">**ADRPARM** structures are used by clients and service providers to control the appearance and behavior of the MAPI common address dialog boxes.</span></span> <span data-ttu-id="4c060-191">Диалоговое окно "адрес" состоит из двух вариантов: немодальных и модальных.</span><span class="sxs-lookup"><span data-stu-id="4c060-191">There are two varieties of the address dialog box: modeless and modal.</span></span> <span data-ttu-id="4c060-192">Некоторые элементы структуры **адрпарм** применяются к обеим версиям диалогового окна, но некоторые из них применимы только к одной из двух версий.</span><span class="sxs-lookup"><span data-stu-id="4c060-192">Some of the members in the **ADRPARM** structure apply to both versions of the dialog box, but some only apply to one of the two versions.</span></span> <span data-ttu-id="4c060-193">В приведенной ниже таблице члены структуры **адрпарм** связаны с их использованием в диалоговых окнах общего адреса.</span><span class="sxs-lookup"><span data-stu-id="4c060-193">The following table relates the members of an **ADRPARM** structure to their use with the common address dialog boxes.</span></span> 
  
|<span data-ttu-id="4c060-194">Элемент АДРПАРМ</span><span class="sxs-lookup"><span data-stu-id="4c060-194">ADRPARM member</span></span>|<span data-ttu-id="4c060-195">Диалоговое окно "тип"</span><span class="sxs-lookup"><span data-stu-id="4c060-195">Type of dialog box</span></span>|
|:-----|:-----|
|<span data-ttu-id="4c060-196">**кбабконтентрид** и **лпабконтентрид**</span><span class="sxs-lookup"><span data-stu-id="4c060-196">**cbABContEntryID** and **lpABContEntryID**</span></span> <br/> |<span data-ttu-id="4c060-197">Модальные и немодальные</span><span class="sxs-lookup"><span data-stu-id="4c060-197">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="4c060-198">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="4c060-198">**ulFlags**</span></span> <br/> |<span data-ttu-id="4c060-199">Модальные и немодальные</span><span class="sxs-lookup"><span data-stu-id="4c060-199">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="4c060-200">**Лпресервед**</span><span class="sxs-lookup"><span data-stu-id="4c060-200">**lpReserved**</span></span> <br/> |<span data-ttu-id="4c060-201">Модальные и немодальные</span><span class="sxs-lookup"><span data-stu-id="4c060-201">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="4c060-202">**улхелпконтекст** и **лпсзелпфиленаме**</span><span class="sxs-lookup"><span data-stu-id="4c060-202">**ulHelpContext** and **lpszHelpFileName**</span></span> <br/> |<span data-ttu-id="4c060-203">Модальные и немодальные</span><span class="sxs-lookup"><span data-stu-id="4c060-203">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="4c060-204">**Лпфнабсди**</span><span class="sxs-lookup"><span data-stu-id="4c060-204">**lpfnABSDI**</span></span> <br/> |<span data-ttu-id="4c060-205">Открыто</span><span class="sxs-lookup"><span data-stu-id="4c060-205">Modeless</span></span>  <br/> |
|<span data-ttu-id="4c060-206">**лпфндисмисс** и **лпвдисмиссконтекст**</span><span class="sxs-lookup"><span data-stu-id="4c060-206">**lpfnDismiss** and **lpvDismissContext**</span></span> <br/> |<span data-ttu-id="4c060-207">Открыто</span><span class="sxs-lookup"><span data-stu-id="4c060-207">Modeless</span></span>  <br/> |
|<span data-ttu-id="4c060-208">**Лпсзкаптион**</span><span class="sxs-lookup"><span data-stu-id="4c060-208">**lpszCaption**</span></span> <br/> |<span data-ttu-id="4c060-209">Модальные и немодальные</span><span class="sxs-lookup"><span data-stu-id="4c060-209">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="4c060-210">**Лпсзневентрититле**</span><span class="sxs-lookup"><span data-stu-id="4c060-210">**lpszNewEntryTitle**</span></span> <br/> |<span data-ttu-id="4c060-211">Модальный</span><span class="sxs-lookup"><span data-stu-id="4c060-211">Modal</span></span>  <br/> |
|<span data-ttu-id="4c060-212">**лпсздествеллститле**, **кдестфиелдс**, **ндестфиелдфокус**, **лппсздесттитлес**и **лпулдесткомпс**</span><span class="sxs-lookup"><span data-stu-id="4c060-212">**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**, and **lpulDestComps**</span></span> <br/> |<span data-ttu-id="4c060-213">Модальный</span><span class="sxs-lookup"><span data-stu-id="4c060-213">Modal</span></span>  <br/> |
|<span data-ttu-id="4c060-214">**Лпконтрестриктион**</span><span class="sxs-lookup"><span data-stu-id="4c060-214">**lpContRestriction**</span></span> <br/> |<span data-ttu-id="4c060-215">Модальные и немодальные</span><span class="sxs-lookup"><span data-stu-id="4c060-215">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="4c060-216">**Лфиеррестриктион**</span><span class="sxs-lookup"><span data-stu-id="4c060-216">**lpHierRestriction**</span></span> <br/> |<span data-ttu-id="4c060-217">Модальные и немодальные</span><span class="sxs-lookup"><span data-stu-id="4c060-217">Modal and modeless</span></span>  <br/> |
   
<span data-ttu-id="4c060-218">Немодальное диалоговое окно — это доступное только для чтения отображение записей из одного или нескольких контейнеров адресных книг.</span><span class="sxs-lookup"><span data-stu-id="4c060-218">The modeless dialog box is a read-only display of entries from one or more address book containers.</span></span> <span data-ttu-id="4c060-219">В диалоговом окне могут отображаться все записи из выбранных контейнеров или только те записи и контейнеры, которые соответствуют условиям, установленным ограничением.</span><span class="sxs-lookup"><span data-stu-id="4c060-219">The dialog box can display all entries from the selected containers or be limited to only those entries and containers that match criteria established by a restriction.</span></span> <span data-ttu-id="4c060-220">Ограничение содержимого, на которое указывает **лпконтрестриктион** , может ограничить типы отображаемых записей, а ограничение иерархии, на которое указывает **лфиеррестриктион** , может ограничить контейнеры, предоставляющие записи.</span><span class="sxs-lookup"><span data-stu-id="4c060-220">The contents restriction pointed to by **lpContRestriction** can limit the types of entries displayed and the hierarchy restriction pointed to by **lpHierRestriction** can limit the containers providing the entries.</span></span> <span data-ttu-id="4c060-221">Чтобы сообщить вызывающему объекту о закрытии диалогового окна, MAPI вызывает функцию, которая предоставляется вызывающей стороной, которая соответствует прототипу [дисмиссмоделесс](dismissmodeless.md) .</span><span class="sxs-lookup"><span data-stu-id="4c060-221">To inform the caller when the dialog box is dismissed, MAPI invokes a function that is provided by the caller that matches the [DISMISSMODELESS](dismissmodeless.md) prototype.</span></span> <span data-ttu-id="4c060-222">Другая функция, которая соответствует прототипу [акцелератеабсди](accelerateabsdi.md) , обеспечивается MAPI и вызывается вызывающим абонентом в цикле обработки сообщений Windows для упрощения работы с сочетаниями клавиш.</span><span class="sxs-lookup"><span data-stu-id="4c060-222">Another function, one that matches the [ACCELERATEABSDI](accelerateabsdi.md) prototype, is provided by MAPI and invoked by the caller in the Windows message loop to facilitate the working of keyboard shortcuts.</span></span> <span data-ttu-id="4c060-223">Немодальная версия диалогового окна "адрес MAPI" может отображаться, когда клиенты вызывают [IAddrBook:: Address](iaddrbook-address.md) или когда поставщики услуг вызывают [Имаписуппорт:: Address](imapisupport-address.md).</span><span class="sxs-lookup"><span data-stu-id="4c060-223">The modeless version of the MAPI address dialog box can be displayed when clients call [IAddrBook::Address](iaddrbook-address.md) or when service providers call [IMAPISupport::Address](imapisupport-address.md).</span></span> 
  
<span data-ttu-id="4c060-224">Модальное диалоговое окно — это отображение записей для чтения и записи из одного или нескольких контейнеров.</span><span class="sxs-lookup"><span data-stu-id="4c060-224">The modal dialog box is a read/write display of entries from one or more containers.</span></span> <span data-ttu-id="4c060-225">Его содержимое может быть затронут аналогично немодальной версии с помощью ограничений, заданные в членах **лпконтрестриктион** и **лфиеррестриктион** .</span><span class="sxs-lookup"><span data-stu-id="4c060-225">Its contents can be affected in the same manner as the modeless version by restrictions set in the **lpContRestriction** and **lpHierRestriction** members.</span></span> <span data-ttu-id="4c060-226">В дополнение к списку, отображающему записи контейнера, модальное диалоговое окно может содержать от одного до трех элементов управления текстовым полем для хранения записей, выбранных пользователем.</span><span class="sxs-lookup"><span data-stu-id="4c060-226">In addition to the list box displaying container entries, the modal dialog box can contain between one and three text box controls for holding entries selected by the user.</span></span> <span data-ttu-id="4c060-227">Каждый элемент управления редактирования связан с определенным типом получателя или свойством **пр_реЦипиент_типе** , таким как мапи_то.</span><span class="sxs-lookup"><span data-stu-id="4c060-227">Each edit control is associated with a particular recipient type or **PR_RECIPIENT_TYPE** property such as MAPI_TO.</span></span> <span data-ttu-id="4c060-228">Диалоговое окно модального адреса может отображаться одним из методов **адреса** или при вызове клиентами [IAddrBook::D етаилс](iaddrbook-details.md) и поставщики услуг вызывают [имаписуппорт::D етаилс](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="4c060-228">The modal address dialog box can be displayed by either of the **Address** methods or when clients call [IAddrBook::Details](iaddrbook-details.md) and service providers call [IMAPISupport::Details](imapisupport-details.md).</span></span> 
  
<span data-ttu-id="4c060-229">Эта иллюстрация включает два элемента управления "текстовое поле", так как элемент **кдестфиелдс** структуры **адрпарм** , управляющий отображением этого диалогового окна, имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="4c060-229">This illustration includes two text box controls because the **cDestFields** member of the **ADRPARM** structure controlling the display of this dialog box is set to 2.</span></span> <span data-ttu-id="4c060-230">Первый элемент управления изначально имеет фокус, так как для элемента **ндестфиелдфокус** задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="4c060-230">The first control has initial focus because the **nDestFieldFocus** member is set to 0.</span></span> 
  
<span data-ttu-id="4c060-231">Элемент **лпсзневентрититле** указывает на текст для подписи кнопки, при выборе которой отображается дополнительное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4c060-231">The **lpszNewEntryTitle** member points to text for a button label that, when it is selected, causes an additional dialog box to be displayed.</span></span> <span data-ttu-id="4c060-232">Как правило, как показано на рисунке модального диалогового окна, кнопка называется **New (создать** ), а в появившемся диалоговом окне — Список всех типов адресов, которые могут создаваться любыми поставщиками адресных книг в профиле.</span><span class="sxs-lookup"><span data-stu-id="4c060-232">Typically, as is shown in the illustration of the modal dialog box, the button is labeled **New** and the dialog box that appears lists all of the types of addresses that can be created by any of the address book providers in the profile.</span></span> <span data-ttu-id="4c060-233">Клиенты вызывают отображение \*\*\*\* этого диалогового окна при вызове метода [IAddrBook:: невентри](iaddrbook-newentry.md) и передает ноль для параметра _кбеидневентритпл_ и значение NULL для параметра _лпеидневентритпл_ , когда пользователь нажимает кнопку.</span><span class="sxs-lookup"><span data-stu-id="4c060-233">Clients cause this **New Entry** dialog box to be displayed by calling [IAddrBook::NewEntry](iaddrbook-newentry.md) and passing zero for the  _cbEidNewEntryTpl_ parameter and NULL for the  _lpEidNewEntryTpl_ parameter when the user selects the button.</span></span> <span data-ttu-id="4c060-234">Сведения, содержащиеся в этом диалоговом окне, берутся из таблицы одноразовых MAPI.</span><span class="sxs-lookup"><span data-stu-id="4c060-234">The information that is included in this dialog box comes from the MAPI one-off table.</span></span> 
  
<span data-ttu-id="4c060-235">Каждая запись в этом диалоговом окне связана с шаблоном для ввода данных, необходимых для создания адреса определенного типа.</span><span class="sxs-lookup"><span data-stu-id="4c060-235">Every entry in this dialog box is associated with a template for entering the data required to create an address of the particular type.</span></span> <span data-ttu-id="4c060-236">Большинство поставщиков адресных книг предоставляют один шаблон для каждого типа записи адресов, который они могут создать.</span><span class="sxs-lookup"><span data-stu-id="4c060-236">Most address book providers supply one template for every type of address entry they can create.</span></span> <span data-ttu-id="4c060-237">Когда пользователь делает выбор из этого диалогового окна, MAPI отображает соответствующий шаблон.</span><span class="sxs-lookup"><span data-stu-id="4c060-237">When a user makes a selection from this dialog box, MAPI displays the corresponding template.</span></span>
  
<span data-ttu-id="4c060-238">Старшие четыре бита элемента **ulFlags** структуры **адрпарм** содержат номер версии, определяющий версию структуры **адрпарм** .</span><span class="sxs-lookup"><span data-stu-id="4c060-238">The most significant four bits of the **ADRPARM** structure's **ulFlags** member contain a version number identifying the version of the **ADRPARM** structure.</span></span> <span data-ttu-id="4c060-239">Текущая версия: 0 (ноль) или АДРПАРМ_ХЕЛП_КТКС.</span><span class="sxs-lookup"><span data-stu-id="4c060-239">The current version is 0 (zero) or ADRPARM_HELP_CTX.</span></span> <span data-ttu-id="4c060-240">Текущая реализация MAPI не будет работать для любой версии структуры, отличной от нуля.</span><span class="sxs-lookup"><span data-stu-id="4c060-240">The current implementation of MAPI will fail for any version of the structure other than zero.</span></span> 
  
<span data-ttu-id="4c060-241">Будущие версии структуры могут быть совершенно другими; они могут не поддерживать структуру нулевой версии.</span><span class="sxs-lookup"><span data-stu-id="4c060-241">Future versions of the structure may be completely different; they may not support the version-zero structure.</span></span> <span data-ttu-id="4c060-242">Следующие макросы предоставляются для извлечения номера версии из члена **ulFlags** и для его объединения с определенными флагами:</span><span class="sxs-lookup"><span data-stu-id="4c060-242">The following macros are provided for extracting the version number from the **ulFlags** member and for combining it with the defined flags:</span></span> 
  
- <span data-ttu-id="4c060-243">**Жет_адрпарм_версион** (_ulFlags_)</span><span class="sxs-lookup"><span data-stu-id="4c060-243">**GET_ADRPARM_VERSION** (_ulFlags_)</span></span> 
- <span data-ttu-id="4c060-244">**Сет_адрпарм_версион** (_ulFlags_, _ улверсион _)</span><span class="sxs-lookup"><span data-stu-id="4c060-244">**SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _)</span></span> 
- <span data-ttu-id="4c060-245">**АДРПАРМ_ХЕЛП_КТКС**</span><span class="sxs-lookup"><span data-stu-id="4c060-245">**ADRPARM_HELP_CTX**</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4c060-246">См. также</span><span class="sxs-lookup"><span data-stu-id="4c060-246">See also</span></span>

- [<span data-ttu-id="4c060-247">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="4c060-247">ACCELERATEABSDI</span></span>](accelerateabsdi.md)
- [<span data-ttu-id="4c060-248">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="4c060-248">DISMISSMODELESS</span></span>](dismissmodeless.md)
- [<span data-ttu-id="4c060-249">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="4c060-249">IAddrBook::Address</span></span>](iaddrbook-address.md)
- [<span data-ttu-id="4c060-250">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="4c060-250">IMAPISupport::Address</span></span>](imapisupport-address.md)
- [<span data-ttu-id="4c060-251">SRestriction</span><span class="sxs-lookup"><span data-stu-id="4c060-251">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="4c060-252">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="4c060-252">MAPI Structures</span></span>](mapi-structures.md)

