---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0d3f540a14c833e0ee0ed212f6f3b3b709d72ec0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591039"
---
# <a name="imapisupportcopymessages"></a>IMAPISupport::CopyMessages

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Копирование или перемещение сообщений из одной папки в другую папку.
  
```cpp
HRESULT CopyMessages(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  LPENTRYLIST lpMsgList,
  LPCIID lpDestInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpSrcInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к папке, содержащей сообщения, чтобы скопировать или переместить.
    
 _lpSrcFolder_
  
> [in] Указатель на папку, содержащую сообщения, чтобы скопировать или переместить.
    
 _lpMsgList_
  
> [in] Указатель на массив идентификаторов записи, чтобы указать сообщения, чтобы скопировать или переместить. 
    
 _lpDestInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к папке назначения для копируемые или перемещения сообщений.
    
 _lpDestFolder_
  
> [in] Указатель на папку назначения для копируемые или перемещения сообщений. Эта папка необходимо открыть.
    
 _ulUIParam_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в _lpProgress_передается значение NULL, поставщика хранилища сообщений отображает индикатор выполнения с помощью реализация объекта MAPI хода выполнения. Параметр _lpProgress_ используется только флаг MESSAGE_DIALOG установлен в _ulFlags_.
    
 _lpProgress_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в _lpProgress_передается значение NULL, поставщика хранилища сообщений отображает индикатор выполнения с помощью реализация объекта MAPI хода выполнения. Параметр _lpProgress_ используется только флаг MESSAGE_DIALOG установлен в _ulFlags_.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как выполнить операцию копирования или перемещения. Можно задать следующие флажки:
    
MESSAGE_DIALOG 
  
> Запрос на отображение индикатор хода выполнения.
    
MESSAGE_MOVE 
  
> Сообщения должны быть перемещены, а не копируются. Если MESSAGE_MOVE не задано, копируются сообщения.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Скопируйте или переместите операция выполнена успешно.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::CopyMessages** реализуется для объектов поддержки поставщика хранилища сообщений. Поставщики хранилища сообщений можно вызвать **IMAPISupport::CopyMessages** в их реализации [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) для копирования или перемещения одно или несколько сообщений из одной папки в другую. Как часть вызова **IMAPISupport::CopyMessages** поставщика хранилища сообщений можно указать, что MAPI должны отображать индикатор хода выполнения. 
  
## <a name="see-also"></a>См. также



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

