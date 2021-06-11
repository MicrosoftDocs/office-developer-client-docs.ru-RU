---
title: IAddrBookSetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424618"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Назначит определенный контейнер в качестве личной адресной книги (PAB).
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор входа контейнера, который будет назначен как PAB. Параметр  _lpEntryID не_ может быть NULL. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Указанный контейнер создан как PAB.
    
## <a name="remarks"></a>Примечания

Клиенты и поставщики услуг звонят по **методу SetPAB,** чтобы назначить определенный контейнер как PAB. PAB — это контейнер, состоящий из записей, скопированные из других контейнеров, а также новых записей. 
  
Вызов в **SetPAB** устанавливает контейнер в качестве PAB до тех пор, пока этот контейнер не станет недоступным или новый контейнер станет PAB с помощью последующего вызова **в SetPAB**. 
  
Чтобы изменить PAB, клиентам и поставщикам не нужно вызывать [метод IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|AbContDlg.cpp  <br/> |CAbContDlg::OnSetPAB  <br/> |MFCMAPI использует **метод SetPAB,** чтобы сделать указанный контейнер PAB.  <br/> |
   
## <a name="see-also"></a>См. также



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Каноническое свойство PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

