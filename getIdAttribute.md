When you have some weird PK's and you have used $model->id all over the place, you can create an accessor to save the day.    
    
    protected $primaryKey = 'ID';
    
    public function getIdAttribute($value)
    {
        return $this->attributes['ID'];
    }
