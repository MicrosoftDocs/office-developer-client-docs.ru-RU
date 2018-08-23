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
ms.openlocfilehash: 2f7e1c131bcdaa19fa4001c0ca566714cfffa456
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571425"
---
# <a name="create-a-simple-mail-item"></a>Создание простого почтового элемента
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
MAPI можно использовать для создания и отправки сообщения, для которого запрашивается прочтении. При запросе прочтении системы обмена сообщениями создает и возвращает чтения отчета отправителю при открытии сообщения получателем.
  
Сведения о загрузке, просмотр и запуск кода из приложения mfcmapi (en) и CreateOutlookItemsAddin проекта, указанного в этом разделе содержатся в разделе [Установка примеров используется в этом разделе](how-to-install-the-samples-used-in-this-section.md).


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a>Создание и отправка сообщения, запрашивающего прочтении

1. Создайте исходящих сообщений. Сведения о создании исходящих сообщений [Исходящих сообщений](handling-an-outgoing-message.md)см.
    
2. Добавьте свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) и задайте для него значение **true**.
    
3. Добавьте свойство **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)).
    
4. Добавьте свойство **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)).
    
5. Отправьте сообщение путем вызова метода [IMessage::SubmitMessage](imessage-submitmessage.md) . 
    
`AddMail` Функции в исходном файле Mails.cpp проекта CreateOutlookItemsAddin демонстрирует следующие действия. `AddMail` Функция принимает параметры в диалоговом окне **Добавление почты** , отображаемое при выборе команды **Добавить почты** в меню **надстройки** в примере приложения mfcmapi (en). `DisplayAddMailDialog` Функция Mails.cpp отображает диалоговое окно и передает значения из диалогового окна `AddMail` функции. `DisplayAddMailDialog` Функция не которые относятся непосредственно к созданию почтового элемента с помощью интерфейса MAPI, поэтому его нет в списке. `AddMail` Функции приведены ниже. 
  
Обратите внимание, что параметр _lpFolder_ , передаваемый `AddMail` метод — это указатель на интерфейс [IMAPIFolder](imapifolderimapicontainer.md) , который представляет папку, где будут создаваться новые сообщения. Учитывая параметр _lpFolder_ , который представляет интерфейс **IMAPIFolder** , код вызывает метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . Метод **CreateMessage** возвращает код успеха и указатель на указатель на [IMessage: IMAPIProp](imessageimapiprop.md) интерфейса. 

Большая часть `AddMail` код функции управляет Установка свойств для вызова метода [IMAPIProp::SetProps](imapiprop-setprops.md) подготовки. При вызове метода **SetProps** завершается успешно, вызов метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) Фиксация изменений в хранилище и создание нового почтового элемента. Затем Если запрос, этот метод [IMessage::SubmitMessage](imessage-submitmessage.md) вызывается для отправки сообщения. 
  
`AddMail` Функция использует две вспомогательные функции для построения значения для свойства **PR_CONVERSATION_INDEX** и **PR_REPORT_TAG** : `BuildConversationIndex` и `AddReportTag` функции. `BuildConversationIndex` Функции, расположенный в CreateOutlookItemsAddin.cpp, не же, встроенную функцию MAPI [ScCreateConversationIndex](sccreateconversationindex.md) выполняет при родительского индекса беседы не передается в нее. Формат буфера беседы индекса, который этих функций описана в [Каноническое свойство PidTagConversationIndex](pidtagconversationindex-canonical-property.md). 

`AddReportTag` Функция, расположенный в Mails.cpp, в свою очередь вызывает `BuildReportTag` функции для создания структуры для свойства **PR_REPORT_TAG** . Сведения о структуре, `BuildReportTag` функции построения [Каноническое свойство PidTagReportTag](pidtagreporttag-canonical-property.md)см.
  
Ниже приведен полный листинг `AddMail` функции. 
  
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

## <a name="see-also"></a>См. также

- [Использование интерфейса MAPI для создания элементов Outlook 2007](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

