---
title: IMAPIFormMgrOpenFormContainer
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
ms.openlocfilehash: 4bf3d9159dd1ed31fb93569218770f1015579339
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582926"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Откроется интерфейс [IMAPIFormContainer](imapiformcontaineriunknown.md) для контейнера конкретной формы. 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Параметры

 _hfrmreg_
  
> [in] Перечисление HFRMREG, которое указывает, библиотека форм, чтобы открыть (то есть, формы контейнер, чтобы открыть). Перечисление HFRMREG является перечислением, характерные для поставщика библиотеки форм. Возможные значения HFRMREG относятся следующие:
    
HFRMREG_DEFAULT 
  
> Контейнер удобное формы.
    
HFRMREG_FOLDER 
  
> Контейнер папки. 
    
HFRMREG_PERSONAL 
  
> Контейнер для хранения сообщений по умолчанию. 
    
HFRMREG_LOCAL 
  
> Контейнер локального формы. 
    
 _lpunk_
  
> [in] Указатель на объект, для которого открывается интерфейс. Параметр _lpunk_ должен быть **значение null** , если значение параметра _hfrmreg_ не требует указателя на объект. 
    
 _lppfcnt_
  
> [out] Указатель на указатель на объект контейнера возвращенные формы.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_INTERFACE 
  
> Объект, на который указывает _lpunk_ не поддерживает необходимый интерфейс. 
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызовите метод **IMAPIFormMgr::OpenFormContainer** для открытия **IMAPIFormContainer** интерфейс для контейнера конкретной формы. Затем этот интерфейс используется для установки в и удаление форм из контейнера формы. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если значение в _hfrmreg_ HFRMREG_FOLDER, идентификатор интерфейса, используемый в _lpunk_ должно быть **значение null** и необходимо иметь возможность вызова метода [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) интерфейс [IMAPIFolder](imapifolderimapicontainer.md) . 
  
Чтобы открыть контейнер локального формы, необходимо использовать вызов метода **OpenFormContainer** или функцию [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) . Чтобы разрешить пользователю выбрать контейнер локальной форме нельзя использовать метод [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) . 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenFormContainer  <br/> |Mfcmapi (en) использует метод **IMAPIFormMgr::OpenFormContainer** для получения контейнером формы, поэтому можно отобразить содержимое контейнера.  <br/> |
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnOpenFormContainer  <br/> |Mfcmapi (en) использует метод **IMAPIFormMgr::OpenFormContainer** для получения контейнером формы для папки, поэтому можно отобразить содержимое контейнера.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

