# iRacingAPIClient

# CAR
## assets
link	https://members-ng.iracing.com/data/car/assets
note	['image paths are relative to https://images-static.iracing.com/']
expirationSeconds	900
get
link	https://members-ng.iracing.com/data/car/get
expirationSeconds	900
CARCLASS
get
link	https://members-ng.iracing.com/data/carclass/get
expirationSeconds	900
CONSTANTS
categories
link	https://members-ng.iracing.com/data/constants/categories
note	Constant; returned directly as an array of objects
expirationSeconds	900
divisions
link	https://members-ng.iracing.com/data/constants/divisions
note	Constant; returned directly as an array of objects
expirationSeconds	900
event_types
link	https://members-ng.iracing.com/data/constants/event_types
note	Constant; returned directly as an array of objects
expirationSeconds	900
HOSTED
combined_sessions
link	https://members-ng.iracing.com/data/hosted/combined_sessions
note	Sessions that can be joined as a driver or spectator, and also includes non-league pending sessions for the user.
parameters	
package_id: (number) If set, return only sessions using this car or track package ID.
expirationSeconds	60
sessions
link	https://members-ng.iracing.com/data/hosted/sessions
note	Sessions that can be joined as a driver. Without spectator and non-league pending sessions for the user.
expirationSeconds	60
LEAGUE
cust_league_sessions
link	https://members-ng.iracing.com/data/league/cust_league_sessions
parameters	
mine: (boolean) If true, return only sessions created by this user.
package_id: (number) If set, return only sessions using this car or track package ID.
expirationSeconds	900
directory
link	https://members-ng.iracing.com/data/league/directory
parameters	
search: (string) Will search against league name, description, owner, and league ID.
tag: (string) One or more tags, comma-separated.
restrict_to_member: (boolean) If true include only leagues for which customer is a member.
restrict_to_recruiting: (boolean) If true include only leagues which are recruiting.
restrict_to_friends: (boolean) If true include only leagues owned by a friend.
restrict_to_watched: (boolean) If true include only leagues owned by a watched member.
minimum_roster_count: (number) If set include leagues with at least this number of members.
maximum_roster_count: (number) If set include leagues with no more than this number of members.
lowerbound: (number) First row of results to return. Defaults to 1.
upperbound: (number) Last row of results to return. Defaults to lowerbound + 39.
sort: (string) One of relevance, leaguename, displayname, rostercount. displayname is owners's name. Defaults to relevance.
order: (string) One of asc or desc. Defaults to asc.
expirationSeconds	900
get
link	https://members-ng.iracing.com/data/league/get
parameters	
league_id: (number)
include_licenses: (boolean) For faster responses, only request when necessary.
expirationSeconds	900
get_points_systems
link	https://members-ng.iracing.com/data/league/get_points_systems
parameters	
league_id: (number)
season_id: (number) If included and the season is using custom points (points_system_id:2) then the custom points option is included in the returned list. Otherwise the custom points option is not returned.
expirationSeconds	900
membership
link	https://members-ng.iracing.com/data/league/membership
parameters	
include_league: (boolean)
expirationSeconds	900
seasons
link	https://members-ng.iracing.com/data/league/seasons
parameters	
league_id: (number)
retired: (boolean) If true include seasons which are no longer active.
expirationSeconds	900
season_standings
link	https://members-ng.iracing.com/data/league/season_standings
parameters	
league_id: (number)
season_id: (number)
car_class_id: (number)
car_id: (number) If car_class_id is included then the standings are for the car in that car class, otherwise they are for the car across car classes.
expirationSeconds	900
season_sessions
link	https://members-ng.iracing.com/data/league/season_sessions
parameters	
league_id: (number)
season_id: (number)
results_only: (boolean) If true include only sessions for which results are available.
expirationSeconds	900
LOOKUP
club_history
link	https://members-ng.iracing.com/data/lookup/club_history
note	Returns an earlier history if requested quarter does not have a club history.
parameters	
season_year: (number)
season_quarter: (number)
expirationSeconds	900
countries
link	https://members-ng.iracing.com/data/lookup/countries
expirationSeconds	900
drivers
link	https://members-ng.iracing.com/data/lookup/drivers
parameters	
search_term: (string) A cust_id or partial name for which to search.
league_id: (number) Narrow the search to the roster of the given league.
expirationSeconds	900
get
link	https://members-ng.iracing.com/data/lookup/get
note	?weather=weather_wind_speed_units&weather=weather_wind_speed_max&weather=weather_wind_speed_min&licenselevels=licenselevels
expirationSeconds	900
licenses
link	https://members-ng.iracing.com/data/lookup/licenses
expirationSeconds	900
MEMBER
awards
link	https://members-ng.iracing.com/data/member/awards
parameters	
cust_id: (number) Defaults to the authenticated member.
expirationSeconds	900
chart_data
link	https://members-ng.iracing.com/data/member/chart_data
parameters	
cust_id: (number) Defaults to the authenticated member.
category_id: (number) 1 - Oval; 2 - Road; 3 - Dirt oval; 4 - Dirt road
chart_type: (number) 1 - iRating; 2 - TT Rating; 3 - License/SR
expirationSeconds	900
get
link	https://members-ng.iracing.com/data/member/get
parameters	
cust_ids: (numbers) ?cust_ids=2,3,4
include_licenses: (boolean)
expirationSeconds	900
info
link	https://members-ng.iracing.com/data/member/info
note	Always the authenticated member.
expirationSeconds	900
participation_credits
link	https://members-ng.iracing.com/data/member/participation_credits
note	Always the authenticated member.
expirationSeconds	900
profile
link	https://members-ng.iracing.com/data/member/profile
parameters	
cust_id: (number) Defaults to the authenticated member.
expirationSeconds	900
RESULTS
get
link	https://members-ng.iracing.com/data/results/get
note	Get the results of a subsession, if authorized to view them. series_logo image paths are relative to https://images-static.iracing.com/img/logos/series/
parameters	
subsession_id: (number)
include_licenses: (boolean)
expirationSeconds	900
event_log
link	https://members-ng.iracing.com/data/results/event_log
parameters	
subsession_id: (number)
simsession_number: (number) The main event is 0; the preceding event is -1, and so on.
expirationSeconds	900
lap_chart_data
link	https://members-ng.iracing.com/data/results/lap_chart_data
parameters	
subsession_id: (number)
simsession_number: (number) The main event is 0; the preceding event is -1, and so on.
expirationSeconds	900
lap_data
link	https://members-ng.iracing.com/data/results/lap_data
parameters	
subsession_id: (number)
simsession_number: (number) The main event is 0; the preceding event is -1, and so on.
cust_id: (number) Required if the subsession was a single-driver event. Optional for team events. If omitted for a team event then the laps driven by all the team's drivers will be included.
team_id: (number) Required if the subsession was a team event.
expirationSeconds	900
search_hosted
link	https://members-ng.iracing.com/data/results/search_hosted
note	Hosted and league sessions. Maximum time frame of 90 days. Results split into one or more files with chunks of results. For scraping results the most effective approach is to keep track of the maximum end_time found during a search then make the subsequent call using that date/time as the finish_range_begin and skip any subsessions that are duplicated. Results are ordered by subsessionid which is a proxy for start time. Requires one of: start_range_begin, finish_range_begin. Requires one of: cust_id, host_cust_id, session_name.
parameters	
start_range_begin: (string) Session start times. ISO-8601 UTC time zero offset: "2022-04-01T15:45Z".
start_range_end: (string) ISO-8601 UTC time zero offset: "2022-04-01T15:45Z". Exclusive. May be omitted if start_range_begin is less than 90 days in the past.
finish_range_begin: (string) Session finish times. ISO-8601 UTC time zero offset: "2022-04-01T15:45Z".
finish_range_end: (string) ISO-8601 UTC time zero offset: "2022-04-01T15:45Z". Exclusive. May be omitted if finish_range_begin is less than 90 days in the past.
cust_id: (number) The participant's customer ID.
host_cust_id: (number) The host's customer ID.
session_name: (string) Part or all of the session's name.
league_id: (number) Include only results for the league with this ID.
league_season_id: (number) Include only results for the league season with this ID.
car_id: (number) One of the cars used by the session.
track_id: (number) The ID of the track used by the session.
category_ids: (numbers) Track categories to include in the search. Defaults to all. ?category_ids=1,2,3,4
expirationSeconds	900
search_series
link	https://members-ng.iracing.com/data/results/search_series
note	Official series. Maximum time frame of 90 days. Results split into one or more files with chunks of results. For scraping results the most effective approach is to keep track of the maximum end_time found during a search then make the subsequent call using that date/time as the finish_range_begin and skip any subsessions that are duplicated. Results are ordered by subsessionid which is a proxy for start time but groups together multiple splits of a series when multiple series launch sessions at the same time. Requires at least one of: season_year and season_quarter, start_range_begin, finish_range_begin.
parameters	
season_year: (number) Required when using season_quarter.
season_quarter: (number) Required when using season_year.
start_range_begin: (string) Session start times. ISO-8601 UTC time zero offset: "2022-04-01T15:45Z".
start_range_end: (string) ISO-8601 UTC time zero offset: "2022-04-01T15:45Z". Exclusive. May be omitted if start_range_begin is less than 90 days in the past.
finish_range_begin: (string) Session finish times. ISO-8601 UTC time zero offset: "2022-04-01T15:45Z".
finish_range_end: (string) ISO-8601 UTC time zero offset: "2022-04-01T15:45Z". Exclusive. May be omitted if finish_range_begin is less than 90 days in the past.
cust_id: (number) Include only sessions in which this customer participated.
series_id: (number) Include only sessions for series with this ID.
race_week_num: (number) Include only sessions with this race week number.
official_only: (boolean) If true, include only sessions earning championship points. Defaults to all.
event_types: (numbers) Types of events to include in the search. Defaults to all. ?event_types=2,3,4,5
category_ids: (numbers) License categories to include in the search. Defaults to all. ?category_ids=1,2,3,4
expirationSeconds	900
season_results
link	https://members-ng.iracing.com/data/results/season_results
parameters	
season_id: (number)
event_type: (number) Retrict to one event type: 2 - Practice; 3 - Qualify; 4 - Time Trial; 5 - Race
race_week_num: (number) The first race week of a season is 0.
expirationSeconds	900
SEASON
list
link	https://members-ng.iracing.com/data/season/list
parameters	
season_year: (number)
season_quarter: (number)
expirationSeconds	900
race_guide
link	https://members-ng.iracing.com/data/season/race_guide
parameters	
from: (string) ISO-8601 offset format. Defaults to the current time. Include sessions with start times up to 3 hours after this time. Times in the past will be rewritten to the current time.
include_end_after_from: (boolean) Include sessions which start before 'from' but end after.
expirationSeconds	60
SERIES
assets
link	https://members-ng.iracing.com/data/series/assets
note	['image paths are relative to https://images-static.iracing.com/']
expirationSeconds	900
get
link	https://members-ng.iracing.com/data/series/get
expirationSeconds	900
past_seasons
link	https://members-ng.iracing.com/data/series/past_seasons
note	Get all seasons for a series. Filter list by official:true for seasons with standings.
parameters	
series_id: (number)
expirationSeconds	900
seasons
link	https://members-ng.iracing.com/data/series/seasons
parameters	
include_series: (boolean)
expirationSeconds	900
stats_series
link	https://members-ng.iracing.com/data/series/stats_series
note	To get series and seasons for which standings should be available, filter the list by official: true.
expirationSeconds	900
STATS
member_bests
link	https://members-ng.iracing.com/data/stats/member_bests
parameters	
cust_id: (number) Defaults to the authenticated member.
car_id: (number) First call should exclude car_id; use cars_driven list in return for subsequent calls.
expirationSeconds	900
member_career
link	https://members-ng.iracing.com/data/stats/member_career
parameters	
cust_id: (number) Defaults to the authenticated member.
expirationSeconds	900
member_division
link	https://members-ng.iracing.com/data/stats/member_division
note	Divisions are 0-based: 0 is Division 1, 10 is Rookie. See /data/constants/divisons for more information. Always for the authenticated member.
parameters	
season_id: (number)
event_type: (number) The event type code for the division type: 4 - Time Trial; 5 - Race
expirationSeconds	900
member_recent_races
link	https://members-ng.iracing.com/data/stats/member_recent_races
parameters	
cust_id: (number) Defaults to the authenticated member.
expirationSeconds	900
member_summary
link	https://members-ng.iracing.com/data/stats/member_summary
parameters	
cust_id: (number) Defaults to the authenticated member.
expirationSeconds	900
member_yearly
link	https://members-ng.iracing.com/data/stats/member_yearly
parameters	
cust_id: (number) Defaults to the authenticated member.
expirationSeconds	900
season_driver_standings
link	https://members-ng.iracing.com/data/stats/season_driver_standings
parameters	
season_id: (number)
car_class_id: (number)
club_id: (number) Defaults to all (-1).
division: (number) Divisions are 0-based: 0 is Division 1, 10 is Rookie. See /data/constants/divisons for more information. Defaults to all.
race_week_num: (number) The first race week of a season is 0.
expirationSeconds	900
season_supersession_standings
link	https://members-ng.iracing.com/data/stats/season_supersession_standings
parameters	
season_id: (number)
car_class_id: (number)
club_id: (number) Defaults to all (-1).
division: (number) Divisions are 0-based: 0 is Division 1, 10 is Rookie. See /data/constants/divisons for more information. Defaults to all.
race_week_num: (number) The first race week of a season is 0.
expirationSeconds	900
season_team_standings
link	https://members-ng.iracing.com/data/stats/season_team_standings
parameters	
season_id: (number)
car_class_id: (number)
race_week_num: (number) The first race week of a season is 0.
expirationSeconds	900
season_tt_standings
link	https://members-ng.iracing.com/data/stats/season_tt_standings
parameters	
season_id: (number)
car_class_id: (number)
club_id: (number) Defaults to all (-1).
division: (number) Divisions are 0-based: 0 is Division 1, 10 is Rookie. See /data/constants/divisons for more information. Defaults to all.
race_week_num: (number) The first race week of a season is 0.
expirationSeconds	900
season_tt_results
link	https://members-ng.iracing.com/data/stats/season_tt_results
parameters	
season_id: (number)
car_class_id: (number)
race_week_num: (number) The first race week of a season is 0.
club_id: (number) Defaults to all (-1).
division: (number) Divisions are 0-based: 0 is Division 1, 10 is Rookie. See /data/constants/divisons for more information. Defaults to all.
expirationSeconds	900
season_qualify_results
link	https://members-ng.iracing.com/data/stats/season_qualify_results
parameters	
season_id: (number)
car_class_id: (number)
race_week_num: (number) The first race week of a season is 0.
club_id: (number) Defaults to all (-1).
division: (number) Divisions are 0-based: 0 is Division 1, 10 is Rookie. See /data/constants/divisons for more information. Defaults to all.
expirationSeconds	900
world_records
link	https://members-ng.iracing.com/data/stats/world_records
parameters	
car_id: (number)
track_id: (number)
season_year: (number) Limit best times to a given year.
season_quarter: (number) Limit best times to a given quarter; only applicable when year is used.
expirationSeconds	900
TEAM
get
link	https://members-ng.iracing.com/data/team/get
parameters	
team_id: (number)
include_licenses: (boolean) For faster responses, only request when necessary.
expirationSeconds	900
TIME_ATTACK
member_season_results
link	https://members-ng.iracing.com/data/time_attack/member_season_results
note	Results for the authenticated member, if any.
parameters	
ta_comp_season_id: (number)
expirationSeconds	900
TRACK
assets
link	https://members-ng.iracing.com/data/track/assets
note	['image paths are relative to https://images-static.iracing.com/']
expirationSeconds	900
get
link	https://members-ng.iracing.com/data/track/get
expirationSeconds	900
