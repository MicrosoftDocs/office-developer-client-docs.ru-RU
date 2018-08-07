---
title: Создание простого почтового элемента
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bbf99c4b-3008-4475-a60a-648eaed59d01
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1bbf80c8f614fc5e69773407c7882f3df8c0c81b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808586"
---
# <a name="create-a-simple-mail-item"></a><span data-ttu-id="1c0da-103">Создание простого почтового элемента</span><span class="sxs-lookup"><span data-stu-id="1c0da-103">Create a simple mail item</span></span>
  
<span data-ttu-id="1c0da-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1c0da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1c0da-105">MAPI можно использовать для создания и отправки сообщения, для которого запрашивается прочтении.</span><span class="sxs-lookup"><span data-stu-id="1c0da-105">MAPI can be used to create and send a message that requests a read receipt.</span></span> <span data-ttu-id="1c0da-106">При запросе прочтении системы обмена сообщениями создает и возвращает чтения отчета отправителю при открытии сообщения получателем.</span><span class="sxs-lookup"><span data-stu-id="1c0da-106">When a read receipt is requested, the messaging system generates and returns a read report to the sender when the recipient opens the message.</span></span>
  
<span data-ttu-id="1c0da-107">Сведения о загрузке, просмотр и запуск кода из приложения mfcmapi (en) и CreateOutlookItemsAddin проекта, указанного в этом разделе содержатся в разделе [Установка примеров используется в этом разделе](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="1c0da-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a><span data-ttu-id="1c0da-108">Создание и отправка сообщения, запрашивающего прочтении</span><span class="sxs-lookup"><span data-stu-id="1c0da-108">To create and send a message requesting a read receipt</span></span>

1. <span data-ttu-id="1c0da-109">Создайте исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="1c0da-109">Create an outgoing message.</span></span> <span data-ttu-id="1c0da-110">Сведения о создании исходящих сообщений [Исходящих сообщений](handling-an-outgoing-message.md)см.</span><span class="sxs-lookup"><span data-stu-id="1c0da-110">For information about how to create an outgoing message, see [Handling an Outgoing Message](handling-an-outgoing-message.md).</span></span>
    
2. <span data-ttu-id="1c0da-111">Добавьте свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) и задайте для него значение **true**.</span><span class="sxs-lookup"><span data-stu-id="1c0da-111">Add the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and set it to **true**.</span></span>
    
3. <span data-ttu-id="1c0da-112">Добавьте свойство **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1c0da-112">Add the **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property.</span></span>
    
4. <span data-ttu-id="1c0da-113">Добавьте свойство **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1c0da-113">Add the **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) property.</span></span>
    
5. <span data-ttu-id="1c0da-114">Отправьте сообщение путем вызова метода [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="1c0da-114">Send the message by calling the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> 
    
<span data-ttu-id="1c0da-115">`AddMail` Функции в исходном файле Mails.cpp проекта CreateOutlookItemsAddin демонстрирует следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1c0da-115">The  `AddMail` function in the Mails.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="1c0da-116">`AddMail` Функция принимает параметры в диалоговом окне **Добавление почты** , отображаемое при выборе команды **Добавить почты** в меню **надстройки** в примере приложения mfcmapi (en).</span><span class="sxs-lookup"><span data-stu-id="1c0da-116">The  `AddMail` function takes parameters from the **Add Mail** dialog box that is displayed when you click the **Add Mail** command on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="1c0da-117">`DisplayAddMailDialog` Функция Mails.cpp отображает диалоговое окно и передает значения из диалогового окна `AddMail` функции.</span><span class="sxs-lookup"><span data-stu-id="1c0da-117">The  `DisplayAddMailDialog` function in Mails.cpp displays the dialog box and passes the values from the dialog box to the  `AddMail` function.</span></span> <span data-ttu-id="1c0da-118">`DisplayAddMailDialog` Функция не которые относятся непосредственно к созданию почтового элемента с помощью интерфейса MAPI, поэтому его нет в списке.</span><span class="sxs-lookup"><span data-stu-id="1c0da-118">The  `DisplayAddMailDialog` function does not relate directly to creating a mail item using MAPI, so it is not listed here.</span></span> <span data-ttu-id="1c0da-119">`AddMail` Функции приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="1c0da-119">The  `AddMail` function is listed below.</span></span> 
  
<span data-ttu-id="1c0da-120">Обратите внимание, что параметр _lpFolder_ , передаваемый `AddMail` метод — это указатель на интерфейс [IMAPIFolder](imapifolderimapicontainer.md) , который представляет папку, где будут создаваться новые сообщения.</span><span class="sxs-lookup"><span data-stu-id="1c0da-120">Note that the  _lpFolder_ parameter passed to the  `AddMail` method is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new message will be created.</span></span> <span data-ttu-id="1c0da-121">Учитывая параметр _lpFolder_ , который представляет интерфейс **IMAPIFolder** , код вызывает метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="1c0da-121">Given the  _lpFolder_ parameter that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="1c0da-122">Метод **CreateMessage** возвращает код успеха и указатель на указатель на [IMessage: IMAPIProp](imessageimapiprop.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1c0da-122">The **CreateMessage** method returns a success code and a pointer to a pointer to an [IMessage : IMAPIProp](imessageimapiprop.md) interface.</span></span> 

<span data-ttu-id="1c0da-123">Большая часть `AddMail` код функции управляет Установка свойств для вызова метода [IMAPIProp::SetProps](imapiprop-setprops.md) подготовки.</span><span class="sxs-lookup"><span data-stu-id="1c0da-123">Most of the  `AddMail` function code handles the work of setting properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="1c0da-124">При вызове метода **SetProps** завершается успешно, вызов метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) Фиксация изменений в хранилище и создание нового почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="1c0da-124">If the call to the **SetProps** method succeeds, a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method commits the changes to the store and creates a new mail item.</span></span> <span data-ttu-id="1c0da-125">Затем Если запрос, этот метод [IMessage::SubmitMessage](imessage-submitmessage.md) вызывается для отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="1c0da-125">Then, if requested, the [IMessage::SubmitMessage](imessage-submitmessage.md) method is called to send the message.</span></span> 
  
<span data-ttu-id="1c0da-126">`AddMail` Функция использует две вспомогательные функции для построения значения для свойства **PR_CONVERSATION_INDEX** и **PR_REPORT_TAG** : `BuildConversationIndex` и `AddReportTag` функции.</span><span class="sxs-lookup"><span data-stu-id="1c0da-126">The  `AddMail` function uses two helper functions to build values for the **PR_CONVERSATION_INDEX** and **PR_REPORT_TAG** properties: the  `BuildConversationIndex` and  `AddReportTag` functions.</span></span> <span data-ttu-id="1c0da-127">`BuildConversationIndex` Функции, расположенный в CreateOutlookItemsAddin.cpp, не же, встроенную функцию MAPI [ScCreateConversationIndex](sccreateconversationindex.md) выполняет при родительского индекса беседы не передается в нее.</span><span class="sxs-lookup"><span data-stu-id="1c0da-127">The  `BuildConversationIndex` function, located in CreateOutlookItemsAddin.cpp, does the same work that the built-in MAPI [ScCreateConversationIndex](sccreateconversationindex.md) function does when a parent conversation index is not passed to it.</span></span> <span data-ttu-id="1c0da-128">Формат буфера беседы индекса, который этих функций описана в [Каноническое свойство PidTagConversationIndex](pidtagconversationindex-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="1c0da-128">The format of the conversation index buffer that these functions generate is documented in [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md).</span></span> 

<span data-ttu-id="1c0da-129">`AddReportTag` Функция, расположенный в Mails.cpp, в свою очередь вызывает `BuildReportTag` функции для создания структуры для свойства **PR_REPORT_TAG** .</span><span class="sxs-lookup"><span data-stu-id="1c0da-129">The  `AddReportTag` function, located in Mails.cpp, in turn calls the  `BuildReportTag` function to build a structure for the **PR_REPORT_TAG** property.</span></span> <span data-ttu-id="1c0da-130">Сведения о структуре, `BuildReportTag` функции построения [Каноническое свойство PidTagReportTag](pidtagreporttag-canonical-property.md)см.</span><span class="sxs-lookup"><span data-stu-id="1c0da-130">For information about the structure that the  `BuildReportTag` function builds, see [PidTagReportTag Canonical Property](pidtagreporttag-canonical-property.md).</span></span>
  
<span data-ttu-id="1c0da-131">Ниже приведен полный листинг `AddMail` функции.</span><span class="sxs-lookup"><span data-stu-id="1c0da-131">The following is the complete listing of the  `AddMail` function.</span></span> 
  
```cpp
HRESULT AddMail(LPMAPISESSION lpMAPISession,
            LPMAPIFOLDER lpFolder,
            LPWSTR szSubject, // PR_SUBJECT_W, PR_CONVERSATION_TOPIC
            LPWSTR szBody, // PR_BODY_W
            LPWSTR szRecipientName, // Recipient table
            BOOL bHighImportance, // PR_IMPORTANCE
            BOOL bReadReceipt, // PR_READ_RECEIPT_REQUESTED
            BOOL bSubmit,
            BOOL bDeleteAfterSubmit)
{
   if (!lpFolder) return MAPI_E_INVALID_PARAMETER;
   HRESULT hRes = S_OK;
   LPMESSAGE lpMessage = 0;
   // Create a message and set its properties
   hRes = lpFolder->CreateMessage(0,
      0,
      &lpMessage);
   if (SUCCEEDED(hRes))
   {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
      SPropValue spvProps[NUM_PROPS] = {0};
      spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag          = PR_MESSAGE_CLASS_W;
      spvProps[p_PR_ICON_INDEX].ulPropTag                 = PR_ICON_INDEX;
      spvProps[p_PR_SUBJECT_W].ulPropTag                = PR_SUBJECT_W;
      spvProps[p_PR_CONVERSATION_TOPIC_W].ulPropTag     = PR_CONVERSATION_TOPIC_W;
      spvProps[p_PR_BODY_W].ulPropTag                   = PR_BODY_W;
      spvProps[p_PR_IMPORTANCE].ulPropTag               = PR_IMPORTANCE;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].ulPropTag   = PR_READ_RECEIPT_REQUESTED;
      spvProps[p_PR_MESSAGE_FLAGS].ulPropTag             = PR_MESSAGE_FLAGS;
      spvProps[p_PR_MSG_EDITOR_FORMAT].ulPropTag         = PR_MSG_EDITOR_FORMAT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].ulPropTag         = PR_MESSAGE_LOCALE_ID;
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].ulPropTag = PR_INETMAIL_OVERRIDE_FORMAT;
      spvProps[p_PR_DELETE_AFTER_SUBMIT].ulPropTag      = PR_DELETE_AFTER_SUBMIT;
      spvProps[p_PR_INTERNET_CPID].ulPropTag            = PR_INTERNET_CPID;
      spvProps[p_PR_CONVERSATION_INDEX].ulPropTag         = PR_CONVERSATION_INDEX;
      spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Note";
      spvProps[p_PR_ICON_INDEX].Value.l = 0x103; // Unsent Mail
      spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
      spvProps[p_PR_CONVERSATION_TOPIC_W].Value.lpszW = szSubject;
      spvProps[p_PR_BODY_W].Value.lpszW = szBody;
      spvProps[p_PR_IMPORTANCE].Value.l = bHighImportance?IMPORTANCE_HIGH:IMPORTANCE_NORMAL;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].Value.b = bReadReceipt?true:false;
      spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_UNSENT;
      spvProps[p_PR_MSG_EDITOR_FORMAT].Value.l = EDITOR_FORMAT_PLAINTEXT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].Value.l = 1033; // (en-us)
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].Value.l = NULL; // Mail system chooses default encoding scheme
      spvProps[p_PR_DELETE_AFTER_SUBMIT].Value.b = bDeleteAfterSubmit?true:false;
      spvProps[p_PR_INTERNET_CPID].Value.l = cpidASCII;
      hRes = BuildConversationIndex(
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.cb,
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb);
      if (SUCCEEDED(hRes))
      {
         hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
         if (SUCCEEDED(hRes))
         {
            hRes = AddRecipient(lpMAPISession,
               lpMessage,
               MAPI_TO,
               szRecipientName);
            AddInLog(true,L"CallMenu: AddRecipient - returned hRes = 0x%08X\n",hRes);
            if (SUCCEEDED(hRes))
            {
               if (bReadReceipt)
               {
                  hRes = AddReportTag(lpMessage);
               }
               if (SUCCEEDED(hRes))
               {
                  hRes = lpMessage->SaveChanges(KEEP_OPEN_READWRITE);
                  if (SUCCEEDED(hRes) && bSubmit)
                  {
                     hRes = lpMessage->SubmitMessage(NULL);
                  }
               }
            }
         }
      }
      if (spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb)
         delete[] spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb;
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}
```

## <a name="see-also"></a><span data-ttu-id="1c0da-132">См. также</span><span class="sxs-lookup"><span data-stu-id="1c0da-132">See also</span></span>

- [<span data-ttu-id="1c0da-133">Использование интерфейса MAPI для создания элементов Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="1c0da-133">Using MAPI to Create Outlook 2007 Items</span></span>](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

