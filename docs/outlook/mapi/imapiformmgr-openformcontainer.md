---
title: Имапиформмгропенформконтаинер
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 68a358c91e35c5a075e220794c78f4e5c96e43ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321639"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает интерфейс [имапиформконтаинер](imapiformcontaineriunknown.md) для определенного контейнера формы. 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Параметры

 _хфрмрег_
  
> возврата Перечисление ХФРМРЕГ, которое указывает открываемую библиотеку форм (то есть, открываемый контейнер формы). Перечисление ХФРМРЕГ — это перечисление, относящееся к поставщику библиотеки форм. Возможные значения ХФРМРЕГ включают следующее:
    
ХФРМРЕГ_ДЕФАУЛТ 
  
> Удобный контейнер форм.
    
ХФРМРЕГ_ФОЛДЕР 
  
> Контейнер папок. 
    
ХФРМРЕГ_ПЕРСОНАЛ 
  
> Контейнер для хранилища сообщений по умолчанию. 
    
ХФРМРЕГ_ЛОКАЛ 
  
> Локальный контейнер форм. 
    
 _лпунк_
  
> возврата Указатель на объект, для которого открыт интерфейс. Параметр _лпунк_ должен иметь **значение NULL** , если для параметра _хфрмрег_ не требуется указатель на объект. 
    
 _лппфкнт_
  
> вышли Указатель на указатель на возвращенный объект контейнера формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
МАПИ_Е_НО_ИНТЕРФАЦЕ 
  
> Объект, на который указывает _лпунк_ , не поддерживает требуемый интерфейс. 
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызывают метод **имапиформмгр:: опенформконтаинер** для открытия интерфейса **имапиформконтаинер** для определенного контейнера формы. Этот интерфейс затем можно использовать для установки форм и удаления форм из контейнера формы. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если значение в _хфрмрег_ — хфрмрег_фолдер, идентификатор интерфейса, используемый в _лпунк_ , должен иметь значение, отличное от **null** , и разрешить вызов метода [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) в интерфейс [IMAPIFolder](imapifolderimapicontainer.md) . 
  
Чтобы открыть локальный контейнер форм, необходимо использовать метод Call для **опенформконтаинер** или функцию [мапиопенлокалформконтаинер](mapiopenlocalformcontainer.md) ; невозможно использовать метод [имапиформмгр:: селектформконтаинер](imapiformmgr-selectformcontainer.md) , чтобы позволить пользователю выбрать локальный контейнер форм. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Маиндлг. cpp  <br/> |Кмаиндлг:: Онопенформконтаинер  <br/> |MFCMAPI использует метод **имапиформмгр:: опенформконтаинер** для получения контейнера формы, чтобы можно было отобразить содержимое контейнера.  <br/> |
|Мсгсторедлг. cpp  <br/> |Кмсгсторедлг:: Онопенформконтаинер  <br/> |MFCMAPI использует метод **имапиформмгр:: опенформконтаинер** для получения контейнера формы для папки, чтобы можно было отобразить содержимое контейнера.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

